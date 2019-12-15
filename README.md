#Data Scrapping using Unity (C#)

Here I have made use of unitys' c# compiler to execute web request using UnityWebRequest library. First a get request
is perfromed on products url i.e. http://18.10.124.57:6000/api/products/ then following data is extracted:

[
    {
        "url": "http://18.10.124.57:6000/api/products/1/",
        "id": 1,
        "title": "My Blanket 1"
    },
    {
        "url": "http://18.10.124.57:6000/api/products/2/",
        "id": 2,
        "title": "My Blanket2"
    }
]

*From the data, url of specific product is again hit with a get request and following data of that product is taken:


{
    "url": "http://18.10.124.57:6000/api/products/1/",
    "id": 1,
    "title": "My Blanket 1",
    "description": "This is the first blanket. And many more",
    "categories": [
        "COATS & JACKETS"
    ],
    "images": [
        {
            "id": 1970,
            "original": "http://18.10.124.57:6000/api/products/1/2019/IMG_1.jpg",
            "product": 1
        },
        {
            "id": 1971,
            "original": "http://18.10.124.57:6000/api/products/1/2019/IMG_2.jpg",
            "product": 1
        },
	{
            "id": 1972,
            "original": "http://18.10.124.57:6000/api/products/1/2019/IMG_3.jpg",
            "product": 1
        }
    ]	
}

*Then as per the category of that instance the images are stored in a persistent data path of the user company name as
defined in player settings. For default, the images are stored in "C:\Users\USERNAME\AppData\LocalLow\DefaultCompany\PROJECTNAME\Images\".

*Folder to store these images has to be named as per the category inside "\Images" folder.

*Then you are all set.