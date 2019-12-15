#Data Scrapping using Unity (C#)

Here I have made use of unitys' c# compiler to execute web request using UnityWebRequest library. 

##Hints
First a get request is perfromed on products url i.e. http://18.10.124.57:6000/api/products/ then following data is extracted:

![Json data of the products]()

From the data, url of specific product is again hit with a get request and following data of that product is taken:

![Json data of images]()

-Then as per the category of that instance the images are stored in a persistent data path of the user company name as
defined in player settings. For default, the images are stored in "C:\Users\USERNAME\AppData\LocalLow\DefaultCompany\PROJECTNAME\Images\".

-Folder to store these images has to be named as per the category inside "\Images" folder.

-Then you are all set.