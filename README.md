# Machine-Learning-Data-Analysis-Graduate-Intern-technical-task

Thank you for applying to Si-Ware Systems. We appreciate the time you take to complete this assignment.

## Assignment
---
At `Si-Ware Systems`, we build the world’s smallest FT-NIR spectrometer, the core technology of our NeoSpectra brand. Our rapidly growing, enthusiastic team thrives in a fast-paced and challenging environment. Together, we’re enabling our customers to get instant, accurate and actionable insights - wherever and whenever they need them.

We aim to build models that are able to predict the percentage of some material properties within a sample. To do so, customers are using our sensors to measure the samples using specific agreed protocol. To ensure that the measurement represent the sample accurately, several readings might be taken per sample. Obviously, this is a human labelling task and hence, prone to human errors. For visual inspection about this process, feel free to see this [video](https://www.youtube.com/watch?v=EW-oE6xRsJs). In addition, the [Youtube channel](https://www.youtube.com/channel/UCPx_Gys4B6hSLw_JY3CkU5w) contains many helpful videos in this context. 

You will be given a real-world dataset that represent a collection of measurments and you are required to do a complete machine learning flow. One necessary requirment is to implement it using Python. After delivering the solution, shortlisted candidates will be invited for a technical discussion. 

It may be divided into the following steps:

  * Build a simple data pipeline that can prepare the data for training and update the model. **It is a good idea to visualize your data before going to the modeling stage.**
  * Build a baseline machine learning model to predict the target value. You may use any framework you are comfortable with. 
  * Analyze the performance of the model. What are some relevant performance metrics?
  * Encaspusalte your model in a way that would make it easier to use by other developers (not necessarliy data scientiests). You can use whatever approach you are comfortable with or find suitable(e.g, dockerfile, package, script+requirments, ...etc.). Define and implement the inference input and the output of your model as part of this step. Given the time constatins, it is not necessary to validate the inputs. 
  
  Kindly, note that developing the best performant ML model is not always required. You shouldn't spend all of your time in the modeling part. The assigment will be graded as a whole. In other words, **pay attention to the analytical skills, documentation and the code clarity.** We are aware that tweaking even a simple ML model is an onerous task that takes time and it might be unnecessary. 

## Deadline
---
You are expected to deliver this assigment within 1 week of recieving.

## Submit Instructions
---

Clone this repo locally and work on your solution. Write `Instructions.md` file to show how to use your solution. When you finish your solution, compress it into a single file and send it by email to `omar.khater@si-ware.com` and put `bassem.mortada@si-ware.com` as CC. Name the file as `<First Name><Last Name> Solution`.

## Datasets
---
Near-infrared spectroscopy (NIRS) is a spectroscopic method that uses the near-infrared region of the electromagnetic spectrum (from 780 nm to 2550 nm). Our application uses only the range (from 1350 nm to 2550 nm). When you apply NIR light to any material, some light is absorbed and some is reflected. The combination of reflected and absorbed light is a characteristic of each material, in other words, like a fingerprint of the matrial.  Reflection is measured with respect to a reference background by dividing the measured reflected light from the sample by the reflected light from the reference material.  Reference material is a material with approximately 99% reflection value through the spectral range. The NIR dataset will contain the IDs of the instrument used in the measurements, the measured material IDs and the reflection value in percentage at each wavelength or wavenumber. Wavenumber is the reciprocal of the wavelength (units in $cm^{-1}$).

You will find **7 NIR tabular datasets** in the data archive. The first row represent the wavenumber vector for each scanner. Each file represents the measurments by a _certain scanner_ on the **same sample set**. Also, there are two reference values columns in the reference sheet.  _You may choose any reference variable_.  


The data columns are described below. 

| Column       | Description |
| ----------- | ----------- |
| First Column     | Label to indicate the measured sample. The label is encoded such that the rightmost number is the reading number while the other numbers are the sample number.|
| Last 257 Columns | Reflection in percentage at specific wavelength/wavenumber. 

Example for label IDs: 

Label: 303
Meaning: First two numbers from left are the sample ID while the last number is the measurements repeating.So, 303 is sample 30 & Measurement 3 for sample 30
