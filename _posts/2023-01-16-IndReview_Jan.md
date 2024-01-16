---
toc: true
comments: true
layout: post
title: Individual Review
description: Reflection and progress
type: plans
courses: { compsci: {week: 2} }
---

Tanisha Patil, Per 3, Overall Individual Review 2023-2024
|                              | Score, Grader Verification |      Blog Link     |        Extras       | Key Indicators: Blog, GitHub File(s) and Key Commits |
|------------------------------|:--------------------------:|:----------------:|:-------------------:|:----------------------------------------------------:|
| SASS hacks                   |               0.89, Toby            |         [LINK](https://tanishapatil1234.github.io/tri2//2023/04/28/P3M-SASSFundamentals_IPYNB_2_.html)         |     Did my own display of SASS (shown in blog) and linked personal website where I implicated SASS lesson fundamentals (Also linked in blog) . **Note**:  Even though I did extra I got the 0.89 because my reflection was not not reflective enough. I do believe the websites that I created with SASS fundamentals from their lesson should count for extra.    <img width="1389" alt="image" src="https://github.com/tanishapatil1234/tri2/assets/111611921/9f24da28-3e2f-4695-9735-038a1e418d38">        |                                                            [Blog Commit](https://github.com/tanishapatil1234/tri2/commit/f4cbdadd5600bf1aae9d31f90efe7b9d7b24b8d6), [Girls in Computer Science Website](https://tanishapatil1234.github.io/girlsincs/) (Created and maintained by me), [SASS Application commit](https://github.com/tanishapatil1234/girlsincs/commit/fd7720a21403d8cff2b0f16c5283ccd11a31aeaf) in my own site |
| jQuery hacks                 |             0.93, Mati               |         [LINK](https://tanishapatil1234.github.io/tri2//2023/12/07/UX_jQuery_CRUD_lesson_IPYNB_2_.html)         |        Created working To-Do list interface, linked on blog  with ALL CURD Functionality, Frontend storage, UI styling, <img width="898" alt="image" src="https://github.com/tanishapatil1234/tri2/assets/111611921/ab385eab-b1d5-4ad2-bbbd-f7f5a0ef844f">|               [Commits](https://tanishapatil1234.github.io/tri2//2023/04/28/P3M-SASSFundamentals_IPYNB_2_.html)                                             |
| Thymeleaf hacks              |           0.94, Krishiv                |      [LINK](https://tanishapatil1234.github.io/tri2//2023/12/12/ThymeLeafLesson_IPYNB_2_.html)            |         Created an extra error page, in depth reflection and hacks        |            [Commits](https://github.com/tanishapatil1234/tri2/actions/runs/7252662837)                                                |
| SQL, HashMap  hacks          |           0.8, Haoxuan  |        [LINK](https://tanishapatil1234.github.io/tri2//2023/12/18/hashlesson_IPYNB_2_.html)          |      No Extras, but I would like to make **Note** : that the reason I got such a low score is because I misunderstood the expectations for the Hashmaps hacks as the lesson was cut short. I did some of my own exploration in hashmaps with a sample application but I didn't do the sports program. I asked if my own code could count for the points but they were only willing to give me up to 0.8               |                                 [Commits](https://github.com/tanishapatil1234/tri2/commit/be59349609b1acbb757ab57ef4f631572fd02271)                         |
| JWT hacks      (OUR LESSON)             |            1, Teacher              |         [Teacher](https://the-zesty-rachits.github.io/CatalinaWarden/2023/12/19/JWTLesson_IPYNB_2_.html) and [Student](https://the-zesty-rachits.github.io/CatalinaWarden/2023/12/19/JWTStudent_IPYNB_2_.html) notebook which I contributed to mosty researching and writing          |         -            |           Researched and Created (most) the lesson(Teacher Notebook) along with Luna, Created all of the student notebook                                |   [LINK](https://tanishapatil1234.github.io/tri2//2023/04/28/P3M-SASSFundamentals_IPYNB_2_.html)    
| CORS, dotEnv, Exploits hacks |          -                  |          -        |              -       |                       -                               |   [LINK](https://tanishapatil1234.github.io/tri2//2023/04/28/P3M-SASSFundamentals_IPYNB_2_.html)    
| CB Quiz                      |        28/39, 1.81/2                 |    [Original Blog](https://tanishapatil1234.github.io/tri2//2023/12/22/CB_MC.html)              |        [ In Depth Blog](https://tanishapatil1234.github.io/tri2//2023/01/07/ReflectionBlog_IPYNB_2_.html), [Extra 5 min lesson on Q 18](https://tanishapatil1234.github.io/tri2//2023/01/16/CB_Lesson_IPYNB_2_.html)         |          [ Commits](https://tanishapatil1234.github.io/tri2//2023/01/07/ReflectionBlog_IPYNB_2_.html)                                              |
|                              |                            |                  |                     |                                                      |
| Totals                       | Median Score:    0.91          | Number complete:  All | Extra effort count:  4 | Key commit count:5                                    |

# pocketTherapist work 
## Sub ticket Tanisha CNN implementation 

### Week 1: Planning and Data Preparation

**Day 0: Sprint Planning**

- [x] - Define the project scope and objectives.
- [x] - Set up a Scrum board or project plan (like this).
- [x] - Kick-off meeting to clarify goals and expectations.

**Day 1: Data Collection**

- [x] Gather a dataset of facial images labeled with emotions ( Kaggle's FER-2013 dataset)
<img width="665" alt="image" src="https://github.com/vivianknee/PocketTherapist/assets/111611921/aefca214-6f59-4975-a5c9-823496d45cf2">

- [x] Clean the dataset by removing irrelevant or low-quality images.
<img width="656" alt="image" src="https://github.com/vivianknee/PocketTherapist/assets/111611921/82e74f42-47f2-4699-a612-115199c22c67">


<img width="538" alt="image" src="https://github.com/vivianknee/PocketTherapist/assets/111611921/442cc8fe-4ad4-489d-b922-6c3ab8c1508b">



**Day 2: Data Preprocessing**

- [x] Resize images to a consistent format (e.g., 224x224 pixels).
> Edit: pre cleaned data set, no need for this!
- [x] Normalize pixel values to a common scale (e.g., [0, 1]).
<img width="302" alt="image" src="https://github.com/vivianknee/PocketTherapist/assets/111611921/7feeee5f-7b9d-4163-a821-dd545566733e">

- [x] Split the dataset into training, validation, and test sets.
- [x] Augment the training dataset (e.g., rotate, flip, zoom) to increase diversity. ENSURE EQUAL DIST. 

<img width="485" alt="image" src="https://github.com/vivianknee/PocketTherapist/assets/111611921/2f132c33-474b-4e9d-b1ce-bef77c663d01">

**Day 3: Model Architecture Design**

- [x] Decide on a CNN architecture (e.g., VGG16, ResNet, or custom architecture).
- [x] Define the layers, filters, and activation functions for the model.
<img width="699" alt="image" src="https://github.com/vivianknee/PocketTherapist/assets/111611921/2d6536c6-3b40-45d7-a1d2-3b170f20ac63">
> Model weights and architecture defined. 

**Day 4: Model Implementation**

- [x] Start coding the CNN model in a deep learning framework like TensorFlow or PyTorch.
- [x] Implement forward and backward passes, loss function, and optimization algorithm (e.g., Adam).
- [x] Ensure the model can handle the input image size and number of classes.

**Day 5: Training**
####(CURRENT)
<img width="699" alt="image" src="https://github.com/vivianknee/PocketTherapist/assets/111611921/6bce9f7e-9584-4c5f-912a-d9799364af4c">

- [x] Train the model on the preprocessed dataset.
- [x] Monitor training metrics such as loss and accuracy.
- [x] Use early stopping if validation performance stalls.
- [x] Document training progress on your Scrum board.

**Day 6: Model Evaluation**

- [x] Evaluate the model's performance using the test set.
- [x] Calculate metrics like accuracy, precision, recall, and F1-score.
- [x] Identify potential sources of bias or error and document them.

### Week 2: Model Optimization and Deployment

**Day 7: Hyperparameter Tuning**

- [x] Fine-tune hyperparameters, like learning rate, batch size, or dropout rates.
- [x] Experiment with different CNN architectures to improve performance.

**Day 8: Error Analysis**

- [x] Analyze model errors on the test set to understand common misclassifications.
- [x] Adjust the model or dataset to address error patterns.

**Day 9: Model Interpretability**

- [x] Implement visualization techniques (e.g., Grad-CAM) to understand what the model focuses on when making predictions.

**Day 10: Model Optimization**

- [x] Implement model optimization techniques (e.g., weight quantization or model pruning) for deployment on resource-constrained devices.

**Day 11: Deployment Setup**

- [x] Set up the infrastructure and environment for model deployment (e.g., cloud server or edge device).
- [x] Create an API or interface for the model.

**Day 12: Testing and Validation**

- [x] Test the deployed model to ensure it functions correctly in the production environment.
- [x] Validate the model's real-world performance.

**Day 13: Documentation and Training**
- [x] Document the model architecture, training process, and deployment steps.
- [x] Train end-users or colleagues on using the model effectively.

**Day 14: Final Review and Retrospective**

- [x] Review the project's achievements and ensure all requirements are met.
- [x] Conduct a retrospective meeting to discuss what went well and what could be improved in the development process.
- [x] Plan for future iterations or improvements.



# ww3 work 
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

### **Commit History** For ww3
Frontend: 
<img width="340" alt="image"  src="https://github.com/rachit-j/ww3/assets/111611921/c9a3fac2-20df-4506-9ca9-0d91f8aa8ec2">
Backend: 
<img width="340" alt="image"  src="https://github.com/rachit-j/ww3/assets/111611921/e37fb7bb-3912-47ac-979b-b46e05017451">


### Retrospective 
I plan to add something like ranks so I could add a compareto method as mentioned by Mort in indicator tech talk. Additionally I would create cards as objects with rank and suit variables instead of using an imperative generation method. However we were sort of in a time crunch because we did ideation incorrectly. 


# Overall 
## Commits 
<img width="705" alt="image" src="https://github.com/tanishapatil1234/tri2/assets/111611921/c3696982-2a74-4e53-a1d5-6dfe3d44be3a">

## Reflection (Bulleted because who wants to read a paragraph) 
- I need to commit more sporadically
- Work on collaboration and task assignment. Take on the role of scrum master and help my team stay on track
- I want to learn automated deployment more in depth (why deploy with the same commands over and over again if I can just learn how to make a deployment script) 
- I want to work with more complicated APIs like AWS or Github to do some interesting data analysis 
- Maybe something like commits/contributions to predict success on live reviews
- I want to try crowd sourcing data for atleast one project this year
- I want to update my personal website with any cool projects I do in this class
- I really want to do the student linkden project on the side 
- I would like to push myself to explore UI, since I spent most of this year focused on using Spring/Flask/Django for backend

