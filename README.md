
# pv-rooftops
Georgetown Data Science PV Rooftops Project

This is a Django project: https://www.djangoproject.com/     
All data is saved to a PostgreSQL relational database.

For more details of the project, check out the research paper ![report](https://github.com/gracelf/PV_Rooftop/blob/master/ResearchPaper.pdf)

How to run the WebSite locally: 
1) Naviagte to Django Web App directory `webapp-google-container-engine`        
2) Install requirements.txt: execute the command `pip install -r requirements.txt`     
3) Execute the command `python manage.py runserver` and Open web browser to load the website 'http://localhost:8000'

Below: a screenshot of the home page  
![](https://github.com/gracelf/PV_Rooftop/blob/master/image/0.jpg)


Below: data pipeline for this project
![](https://github.com/gracelf/PV_Rooftop/blob/master/image/1.jpg)


Below: API to predicted the market growth (input: year and installation price)
![](https://github.com/gracelf/PV_Rooftop/blob/master/image/2.jpg)


![](https://github.com/gracelf/PV_Rooftop/blob/master/image/3.jpg)


![](https://github.com/gracelf/PV_Rooftop/blob/master/image/4.jpg)

   

How to run the API locally: 
1) Naviagte to Django API directory `django_pv` and execute the command `python manage.py runserver`
     -- The DIRS[] settting of the TEMPLATES configuration in `django_pv/settings.py` may have to be changed to read `'DIRS': ['pv/templates'],` 
2) Open web browser and type `http://localhost:8000/pv/?year=#&price=#` replacing #'s with desired variable.
     -- For years <= 2015, pre-extracted, non-predicted values will be used. Everything else is predicted by national isntallation price per watt.
3) Please update requirements.txt as necessary
