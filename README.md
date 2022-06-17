# Emotional Mario Readme

> environment setting

### 1. create conda env
```
conda env create -f EmotionalMario.yml
```

### 2. find where the tesseract execution file is in and paste it into the code
after you create conda env, pytesseract and tesseract should have been installed now in your env.  
you are able to find the tesseract execution file by input this: 
```
where tesseract
```

### 3. put our trained data in tessdata folder

### 4. setting environment variables
a. TESSDATA_PREFIX  
b. %TESSDATA%

### 5. run the code

