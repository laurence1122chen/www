# Emotional Mario Readme

> environment setting

### 1. create conda env and activate it
```
conda env create -f EmotionalMario.yml
```
```
conda activate EmotionalMario
```

### 2. find where the tesseract execution file is in and paste it into the code
after you create and activate conda env, pytesseract and tesseract should have been installed now in your env.  
you are able to find the tesseract execution file by input this: 
```
where tesseract
```
example output : "C:\Users\tronu\Anaconda3\envs\EmotionalMario\Library\bin\tesseract.exe"  
you should put this path in line 23 of our code.  
*note : if you have already installed tesseract, there can be not 1 path in output. just pick up one under our "EmotionalMario" env.  
it will look like:   
pytesseract.pytesseract.tesseract_cmd = r'[tesseract execution file path]' 
![](https://i.imgur.com/qLYUmbW.png)

*if you can not find the path by instruction above, try to install by using this:
```
 conda install -c conda-forge pytesseract
```
```
 conda install -c conda-forge tesseract
```
and find the path again
```
where tesseract
```

### 3. put our trained data in tessdata folder
you can find where your env folder is at by using the output above.  
For example, if the path is "C:\Users\tronu\Anaconda3\envs\EmotionalMario\Library\bin\tesseract.exe", you can enter "C:\Users\tronu\Anaconda3\envs\EmotionalMario",
and you will see a "share" folder, enter it.
![](https://i.imgur.com/ZTWmYcQ.png)
then you will see a "tessdata" folder, just **put our trained data "mario.traineddata" into "tessdata" folder**.
![](https://i.imgur.com/iaucwZs.png)
and you should remember or copy the path of tessdata, which will be used in step 4.
example path: "**C:\Users\tronu\Anaconda3\envs\EmotionalMario\share\tessdata**"

### 4. setting environment variables
you can search in your computer using "environment variables" or "環境變數" as key word.  
![](https://i.imgur.com/5Syi5fk.png)  
click "環境變數".  
![](https://i.imgur.com/s4pBWpt.png)  
a. TESSDATA_PREFIX  
    add a system variable "**TESSDATA_PREFIX**" which value is the path you copied in step 3.  
    ![](https://i.imgur.com/grNR2Bm.png)
    (I have already created it before, so you will see it in the picture )
    ![](https://i.imgur.com/li7ATm4.png)
b. %TESSDATA_PREFIX%
    and double click , or just edit the system variable "Path" by adding a value "**%TESSDATA_PREFIX%**"
    ![](https://i.imgur.com/jiKnQ9Y.png)
    ![](https://i.imgur.com/2TsKvf3.png)

### 5. run the code
if you have completed all the step above, you can run our code by this:
```
python model.py -p [path of the "participants" folder] -i [number of participant] -o [output file path]
```
just similar to baseline.py.
here is an example:
**python model.py -p C:\Users\tronu\OneDrive\桌面\toadstool\toadstool\participants -i 0 -o C:\Users\tronu\OneDrive\桌面\ouput_folder**
and you will be able to see the csv ouput file in [output file path]

