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
lakepark.html
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lake park</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
        }
        header {
            background:beige;
            color: white;
            padding: 20px 0;
            text-align: center;
        }
        nav {
            margin: 20px 0;
        }
        nav a {
            margin: 0 15px;
            color:beige;
            text-decoration: none;
        }
        main {
            padding: 20px;
        }
        section {
            margin-bottom: 20px;
            background: white;
            padding: 15px;
            border-radius: 5px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }
        footer {
            text-align: center;
            padding: 10px;
            background: #2c3e50;
            color: white;
            position: relative;
            bottom: 0;
            width: 100%;
        }
    </style>
</head>
<body>



<main>
    <section id="about">
        <img src=C:\Users\Suriya\Desktop\workspace\imagemapping\app\static\park.jpg alt="gn">
        <h2>Avadi lake park</h2>
        <p>Avadi Lake lies right behind the Tamil Nadu Housing Board (TNHB) and Thirumullaivoyal. This lake is of length of 2.64 kilometers and covers an area of 8 acres before the restoration.[3] It is mostly known to have never dried up in many years. This lake has supposedly been a source of water for cultivation of farm lands long before. The water body attracts many birds during various seasons.

            The lake is fed by surplus water from the unpolluted stretch of the Cooum River.[1] The lake serves as a source for groundwater recharge in the neighbouring areas, such as Adhiparasakthi Nagar and Govardhanagiri.[6] The average depth is 12 feet.[5]
            
            However, in recent decades the lake has lost most of its area to indiscriminate building and encroachment. These are the major problems at present, since the water of the monsoon showers moves inside of the buildings as they are in the area of the lake.[7]</p>
    </section>

</body>
</html>
```
railwaystation.html
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lake park</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
        }
        header {
            background:beige;
            color: white;
            padding: 20px 0;
            text-align: center;
        }
        nav {
            margin: 20px 0;
        }
        nav a {
            margin: 0 15px;
            color:beige;
            text-decoration: none;
        }
        main {
            padding: 20px;
        }
        section {
            margin-bottom: 20px;
            background: white;
            padding: 15px;
            border-radius: 5px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }
        footer {
            text-align: center;
            padding: 10px;
            background: #2c3e50;
            color: white;
            position: relative;
            bottom: 0;
            width: 100%;
        }
    </style>
</head>
<body>



<main>
    <section id="about">
        <img src=C:\Users\Suriya\Desktop\workspace\imagemapping\app\static\station.jpg alt="gn">
        <h2>Avadi Railway Station</h2>
        <p>Avadi railway station (station code: AVD[3]) is an NSG–2 category Indian railway station in Chennai railway division of Southern Railway zone.[3] It is one of the major railway terminals of the Chennai Central–Arakkonam section of the Chennai Suburban Railway Network. It serves the neighbourhood of Avadi, a suburb of Chennai located 23 km west of the city centre. It is situated at Tirumalairajapuram locality of Avadi, with an elevation of 26.85 m above sea level. According to a railway release in 2008, there are plans to develop Avadi station as a coaching terminal (satellite terminal) for Chennai Central railway station, on the lines of Tambaram station being developed as a terminal for Egmore railway station.[4] Later in 2023, the plans of making Avadi, Ambattur or Villivakkam as terminal were dropped, and Perambur was chosen for development of terminal station.</p>
    </section>

</body>
</html>
```
tidel park.html
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>LTidle park</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
        }
        header {
            background:beige;
            color: white;
            padding: 20px 0;
            text-align: center;
        }
        nav {
            margin: 20px 0;
        }
        nav a {
            margin: 0 15px;
            color:beige;
            text-decoration: none;
        }
        main {
            padding: 20px;
        }
        section {
            margin-bottom: 20px;
            background: white;
            padding: 15px;
            border-radius: 5px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }
        footer {
            text-align: center;
            padding: 10px;
            background: #2c3e50;
            color: white;
            position: relative;
            bottom: 0;
            width: 100%;
        }
    </style>
</head>
<body>



<main>
    <section id="about">
        <img src=C:\Users\Suriya\Desktop\workspace\imagemapping\app\static\tidel-pattabiram.jpg alt="gn">
        <h2>Tidle park avadi</h2>
        <p>TIDEL Park, Chennai has established an Information Technology Park with built up space of  5.57lakh sq. ft in an area of 11.41 acres of land in Pattabiram village, Avadi Taluk. The IT Hub was grandly inaugurated on 22.10.2024 by Hon’ble CM of Tamil Nadu Thiru. MK Stalin.

            The inaugurated Information Technology (IT) Park - TIDEL Park Pattabiram is situated at Avadi with a view to contribute and develop the socio economic development in the North Western part of Chennai City.
            
            This New TIDEL in Pattabiram is a 21-storey facility with various amenities and facilities such as 100% DG backup, open car parking, a multi-cuisine food court, auditorium, promotional spaces, a fully equipped gym, meditation hall, indoor games, EV charging stations and a medical center. This IT hub ensures 24/7 security surveillance, CCTV monitoring, with an Integrated Building Management system.
            
            The IT Hub will act as the address for start-ups, and enterprises in the IT/ITeS sector with the potential of providing job opportunities to 6000 IT employees in its first phase,  it offers flexible office spaces ranging from 6,000 sq. ft. to 1 lakh sq. ft., meeting the needs of diverse businesses.</p>
    </section>

</body>
</html>
```
hvf.html
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HVF</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
        }
        header {
            background:beige;
            color: white;
            padding: 20px 0;
            text-align: center;
        }
        nav {
            margin: 20px 0;
        }
        nav a {
            margin: 0 15px;
            color:beige;
            text-decoration: none;
        }
        main {
            padding: 20px;
        }
        section {
            margin-bottom: 20px;
            background: white;
            padding: 15px;
            border-radius: 5px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }
        footer {
            text-align: center;
            padding: 10px;
            background: #2c3e50;
            color: white;
            position: relative;
            bottom: 0;
            width: 100%;
        }
    </style>
</head>
<body>



<main>
    <section id="about">
        <img src=C:\Users\Suriya\Desktop\workspace\imagemapping\app\static\HVF-Heavy-Vehicle-Factory.jpg alt="gn">
        <h2>Tidle park avadi</h2>
        <p>Heavy Vehicles Factory (HVF) is an armoured vehicle and battle tank manufacturing factory located at Avadi in Chennai in the Indian state of Tamil Nadu. It is managed by Armoured Vehicles Nigam Limited (AVANI) of the Ministry of Defence, Government of India.[1]</p>
    </section>

</body>
</html>
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

