---
toc: true
comments: true
layout: post
title: WW3  ~ Tanisha accomplishments 
description: Plans/ideation 
type: tangibles
courses: { compsci: {week: 0} }
---

### Demo/Summary Video 
[Youtube Link](https://youtu.be/zwe7Q_r6jEE)

### **Creating Backend Endpoints - Backend**
- My contributions in java was setting up and creating the backend api. This is meant to contain all of the cards, or data in our project. 
- CardGeneration, Service , controller, main, jpa repository, classes
- One improvement that was suggested in an earlier review was to create a larger dataset to demonstrate the varying complexities of the sorting algorithms better, so I changed the dataset from containing 52 records (like a deck) to 500 cards. 

Generation and Service Classes: 
```
@Configuration
public class CardGeneration {

    @Bean
    CommandLineRunner commandLineRunner(
        CardJpaRepository repository) {
            return args -> {
            List<Card> cards = new ArrayList<>();

            for (int rank = 1; rank <= 500; rank++) {
                Card card = new Card(rank);
                cards.add(card);
            }

            repository.saveAll(cards);
        };
        }
```

```

@Service
public class CardService {

    private final CardJpaRepository cardRepository;

    @Autowired
    public CardService(CardJpaRepository cardRepository) {
        this.cardRepository = cardRepository;
    }

    public List<List<Card>> splitCardsRandomly(List<Card> cards) {
        // Shuffle the cards randomly
        Collections.shuffle(cards);

        // Split the cards into two halves
        int halfSize = cards.size() / 2;

        List<Card> firstHalf = new ArrayList<>(cards.subList(0, halfSize));
        List<Card> secondHalf = new ArrayList<>(cards.subList(halfSize, cards.size()));

        List<List<Card>> splitCards = new ArrayList<>();
        splitCards.add(firstHalf);
        splitCards.add(secondHalf);

        return splitCards;
    }
// commit change 

    public void saveCards(List<Card> cards) {
        cardRepository.saveAll(cards);
    }
}
    
```

- Java Fundamental: class extension can be seen in JPA repository file. JPA repository is an interface which is a part of the Spring Data repository support and provides methods for common database operations (like save, delete, findById, etc.) without the need for manual implementation. The use of this class extension was very helpful!

```
@Repository
public interface CardJpaRepository extends JpaRepository<Card, Long> {
    void save(String Card); 
    List<Card> findByIdIgnoreCase(Long id);
} 
```


Endpoint: 
<img width="340" alt="image" src="https://github.com/rachit-j/ww3/assets/111611921/32634758-84f5-486e-8881-a31b09349c90">

Postman: 
<img width="340" alt="image" src="https://github.com/rachit-j/ww3/assets/111611921/4e17c1e8-4b55-41b0-9a7d-3bc553189842">

[Key Commit Backend
](https://github.com/rachit-j/ww3-backend/commits?author=tanishapatil1234)


### **Creating Test Analysis File - Frontend**
- I also created this analysis file on the frontend order to do testing calls with my backend endpoints. 
- The testing I did with my api, was incorporated into the final sorting file. 

<img width="340" alt="image" src="https://github.com/rachit-j/ww3/assets/111611921/849f81a4-6e78-4a6d-935b-e1c8601a9ba6">

- [Link](https://rachit-j.github.io/ww3/testanalysis/) to testing file 


[Key Commit Frontend
](https://github.com/rachit-j/ww3/commits?author=tanishapatil1234)

### **Commit History**
Frontend: 
<img width="340" alt="image"  src="https://github.com/rachit-j/ww3/assets/111611921/c9a3fac2-20df-4506-9ca9-0d91f8aa8ec2">
Backend: 
<img width="340" alt="image"  src="https://github.com/rachit-j/ww3/assets/111611921/e37fb7bb-3912-47ac-979b-b46e05017451">


### Retrospective 
I plan to add something like ranks so I could add a compareto method as mentioned by Mort in indicator tech talk. Additionally I would create cards as objects with rank and suit variables instead of using an imperative generation method. However we were sort of in a time crunch because we did ideation incorrectly. 
