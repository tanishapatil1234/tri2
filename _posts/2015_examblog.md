---
toc: true
comments: true
layout: post
title: CB MCQ 2015
description: Reflection on MCQ
type: plans
courses: { compsci: {week: 2} }
---
# Score Proof 
![image](https://github.com/nighthawkcoders/teacher_portfolio/assets/111611921/09480ff4-428c-47ae-be9a-151ec77d34fe)

# Reflection 
| Question  | Correct Answer | Reasoning |
|:---:|---|:---:|
| <img width="957" alt="image" src="https://github.com/tanishapatil1234/student/assets/111611921/a7c1a959-e828-4904-a6de-b37406d8f1fe"> | D | In the first iteration, k = 0 o result[ai.length - 1] is a2[0] which means the value of a1[a1.length - 1] will not be in result. The right answer is D because all the values from a1 are copied to result (at the corresponding indices). Then the first index where the first element of a2 should be copied into is a1.length. This is why k + ai.length accesses all corresponding elements in result.  |
| <img width="512" alt="image" src="https://github.com/tanishapatil1234/student/assets/111611921/4bfb0066-4096-4dc5-836b-303e61379b0e">| C | A is incorrect because it would be the result of the array if arr[k+1] didn't update every element.  In the first iteration, when k is 3, arr[3] is assigned the value arr[4]. As k is incremented to 6,  the loop terminates and the doubled value will be the last one (7) |
| <img width="512" alt="image" src="https://github.com/tanishapatil1234/student/assets/111611921/03b463a0-6722-4014-b19b-34c971dcd5b9"> | C | Passing a reference parameter results in the formal parameter being aliases with the actual parameter, meaning that they both refer to the same object. So any update made to the referenced array is being made on an array referenced by both data and values. So, when data[k+1] is updated, the value new value should be ussed.  |