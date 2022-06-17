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
after you create conda env, pytesseract and tesseract should have been installed now in your env.  
you are able to find the tesseract execution file by input this: 
```
where tesseract
```
example output : "C:\Users\Peter\Anaconda3\envs\tesseract\Library\bin\tesseract.exe" <-- 之後改掉  
you should put this path in line 23 of our code  
it will look like 
pytesseract.pytesseract.tesseract_cmd = [tesseract execution file path]  
[image] <-- 之後加

*if you can not find the path by instruction above, try to install by this:
```
 conda install -c conda-forge pytesseract
```
```
 conda install -c conda-forge tesseract
```

### 3. put our trained data in tessdata folder

### 4. setting environment variables
a. TESSDATA_PREFIX  
b. %TESSDATA%

### 5. run the code

