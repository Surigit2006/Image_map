# Ex04 Places Around Me
# Date:
# AIM
To develop a website to display details about the places around my house.

# DESIGN STEPS
## STEP 1
Create a Django admin interface.

## STEP 2
Download your city map from Google.

## STEP 3
Using <map> tag name the map.

## STEP 4
Create clickable regions in the image using <area> tag.

## STEP 5
Write HTML programs for all the regions identified.

## STEP 6
Execute the programs and publish them.

# CODE
templates
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Avadi</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 20px;
            background-color: #f4f4f4;
        }
        .title {
            text-align: center;
            margin-bottom: 20px;
        }
        .imagemap {
            position: relative;
            width: 600px; /* Adjust as needed */
            margin: 0 auto; /* Center the image map */
        }
        .imagemap img {
            width: 100%;
            height: auto;
        }
        
        
    </style>
</head>
<body>
    <h1 class="title">Avadi</h1>
    <p style="text-align:center;">imagemapping by M.K.Suriya prakash</p>
    <div class="imagemap">
        {% load static %}
        <img src="{% static 'map.png' %}" alt="Image Map Example">
        <!-- Define clickable areas -->
        <a href="c:\Users\Suriya\Desktop\Untitled-4.html" class="area" style="top: 50px; left: 100px; width: 100px; height: 100px;"></a>
        <a href="c:\Users\Suriya\Desktop\station.html" class="area" style="top: 200px; left: 300px; width: 150px; height: 150px;"></a>
        <a href="c:\Users\Suriya\Desktop\tidel park.html" class="area" style="top: 50px; left: 100px; width: 100px; height: 100px;"></a>
        <a href="c:\Users\Suriya\Desktop\hvf.html" class="area" style="top: 200px; left: 300px; width: 150px; height: 150px;"></a>
    </div>
</body>
</html>
```
views.py
```
from django.shortcuts import render

def imagemap(request):
    return render(request, 'imagemapping.html')
```
urls.py
```
from django.contrib import admin
from django.urls import include, path
from app import views

urlpatterns = [
    # path("", include("app.urls")),
    path('admin/', admin.site.urls),
    path('imagemapping/',views.imagemap),]
```



# OUTPUT
![Screenshot 2024-12-23 001724](https://github.com/user-attachments/assets/e07d84c1-0623-41f4-be3f-c710bdb0c5fa)
![Screenshot 2024-12-22 235631](https://github.com/user-attachments/assets/d33b5e84-47a7-4b24-90d9-c72d9fe4532e)
![Screenshot 2024-12-22 235648](https://github.com/user-attachments/assets/d5727749-4881-4f03-87e8-d81830fa131f)
![Screenshot 2024-12-23 001747](https://github.com/user-attachments/assets/76e754e0-64f9-4c8a-9cff-e2a1e2543270)
![Screenshot 2024-12-23 001803](https://github.com/user-attachments/assets/f8ad4827-65b0-49c2-b597-3aebe7d5e590)
![Screenshot 2024-12-23 001401](https://github.com/user-attachments/assets/d196d42f-f93b-45c0-ab78-3472e0dd248b)

# RESULT
The program for implementing image maps using HTML is executed successfully.

