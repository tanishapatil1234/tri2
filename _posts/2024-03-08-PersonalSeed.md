---
comments: true
layout: post
title: Personal Seed
permalink: debug
unit: 2
---

# Individual Progress

## Organization 
<img width="783" alt="image" src="https://github.com/tanishapatil1234/tri2/assets/111611921/4a5a8d6f-9ee0-4a37-9d70-442542b1635e">


## Ap Prep Progress
I worked in much detail to finish these frqs. Each frq I related to my personal project. This was important as PBL application helped me understand unclear CB topics. 

| FRQ | Link |
|---|---|
| 1 | [link](https://tanishapatil1234.github.io/tri2//2024/02/25/frq1_IPYNB_2_.html) |
| 2 | [link](https://tanishapatil1234.github.io/tri2//2024/02/25/frq2_IPYNB_2_.html) |
| 3 | [link](https://tanishapatil1234.github.io/tri2//2024/02/25/frq3_IPYNB_2_.html) |
| 4 | [link](https://tanishapatil1234.github.io/tri2//2024/02/25/frq4_IPYNB_2_.html) |


## Key Commits
**Pocket Therapist**
- [AI Work](https://tanishapatil1234.github.io/tri2//2023/01/18/ww3personal.html)
- [Backend Construction](https://tanishapatil1234.github.io/tri2//2023/01/18/ww3backend.html)
- [Key Commits ~ Frontend](https://github.com/vivianknee/PocketTherapist/commits?author=tanishapatil1234)
> Constructed camera and camera container. Frontend also holds code for the javascript OpenCV work
- [Key Commits ~ Backend](https://github.com/vivianknee/PT_Backend/commits?author=tanishapatil1234)
> Constructed the entire quotes database on Spring



**WW3 Mini Project**
- [All Accomplishments](https://tanishapatil1234.github.io/tri2//2023/01/18/worldwarplan.html)
- [Key Commits ~ Frontend](https://github.com/rachit-j/ww3/commits?author=tanishapatil1234)
> Constructed testing file where I worked to integrate backend requests of cards into sorting algos. 
- [Key Commits ~ Backend](https://github.com/rachit-j/ww3-backend/commits?author=tanishapatil1234) . 
> Constructed the entire cards database on Spring


**Personal Project** 
- This is a model I created to forecast power voltage generation of a solar panel based on imaging data of weather conditions. It is a deep learning model I am building in pytorch, and an expansion on a very vague research paper done by professors at Stanford and Upenn. 
- I have background in AI and machine learning but when I was preprocessing my data, I decided to utilize a class based approach to hone in my skills from this class into my own project. So even though my model is HUGE (13 million parameters as of now) it is able to utilize getter functions that I wrote efficiently 
- I do not have it committed yet because of liscencing issues I am trying to navigate, but here is some code 

<code>
class ImageDataset(Dataset):
    def __init__(self, h5_file, group, transform=None, target_transform=None):
        self.h5_file = h5_file
        self.group = group
        self.transform = transform
        self.target_transform = target_transform

        with h5py.File(h5_file, 'r') as f:
            images = f[self.group]['images_log'][:]
            labels = f[self.group]['pv_log'][:]

        self.images = images
        self.labels = labels
    
    def __len__(self):
        return len(self.images)

    def convert_to_float32(self, image, label):
        image = ((image - image.min()) / (image.max() - image.min()) * 255).astype(np.uint8)
        return image.astype(np.float32), label.astype(np.float32)

    def __getitem__(self, idx):
        image = self.images[idx]
        label = self.labels[idx]

        # Convert to float32
        image, label = self.convert_to_float32(image, label)

        if self.transform:
            image = (image * 255).astype(np.uint8)
            image = self.transform(image)

        if self.target_transform:
            label = self.target_transform(label)

        return image, label
</code>

**Tri 2 Continuing Project** 
<img width="888" alt="image" src="https://github.com/tanishapatil1234/tri2/assets/111611921/977bb16e-db2e-42a1-941c-28428aea36ae">

Main Commit: 
[LINK](https://github.com/Codemaxxers/codemaxxerFrontend/commit/0d733b1e73b3769dac86ca876295836454fcb973)

Blog Detailing Main Commit: [LINK](https://tanishapatil1234.github.io/tri2//2024/02/02/GamingInJava_IPYNB_2_.html)


## Github Analytics
<img width="672" alt="image" src="https://github.com/tanishapatil1234/tri2/assets/111611921/cb258d36-1d59-43cc-b857-7e7d741c8cdc">

## Personal Spotlight
- I need to commit more sporadically
- Work on collaboration and task assignment. Take on the role of scrum master and help my team stay on track
- I want to learn automated deployment more in depth (why deploy with the same commands over and over again if I can just learn how to make a deployment script)
- I want to work with more complicated APIs like AWS or Github to do some interesting data analysis
- Maybe something like commits/contributions to predict success on live reviews
- I want to try crowd sourcing data for atleast one project this year
- I want to update my personal website with any cool projects I do in this class
- I really want to do the student linkden project on the side
- I would like to push myself to explore UI, since I spent most of this year focused on using Spring/Flask/Django for backend

## GitHub Blog

[LINK](https://tanishapatil1234.github.io/tri2/compsci)

## Project Work
Up to this point, I've been enjoying the camaraderie within my group. They've been instrumental in aiding my comprehension of challenging concepts, and together, we maintain mutual accountability for our respective tasks. Our frequent communication, often through facetimes, ensures that we are well-prepared for upcoming activities and assignments.






