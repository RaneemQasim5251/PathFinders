# PathFinders
Our model aims to predict the paths most at risk of collision with debris to avoid them.

# Background
Since the first satellite deployment in 1958 with  Sputnik 1 , the rate of deployment has increased significantly. Today, more than 500 satellites are deployed annually, and this figure is expected to increase by 140% by 2025. Currently, there are over 12,000 satellites orbiting Earth; 4,900 of which are active. SpaceX's long-term plan is to launch more than  42,000 Starlink satellites , and other companies will follow suit. One issue standing in the way of this future is the extensive collection of space debris that circles the Earth at speeds in excess of 15,000 miles per hour. Collisions between orbiting bodies have obvious negative effects on infrastructure on Earth, but it has even larger consequences that could prevent humanity from ever venturing into space again.

# Kessler Syndrome
When a satellite collides with space debris, it doesn't slow down and fall back to Earth. Because there is no downward acceleration, collisions cause satellites to fragment into smaller pieces that travel even faster due to the  law of conservation of momentum . These fragments can then collide with more space debris creating more fragments. This exponential collision cascade is known as  Kessler Syndrome . It is currently estimated that there are  10,000 pieces of space debris the size of a monitor, 20,000 pieces the size of a baseball, 500,000 pieces the size of a marble, and over 100,000,000 pieces too small to be tracked.


![shakti](https://github.com/RaneemQasim5251/PathFinders/assets/108181104/3fb7fbb9-09d1-41ba-92f7-f3cea18bfac4)



*Graphical representation of Kessler Syndrome (USRadioguy.com, 2021).*



![Space_debris_GIF](https://github.com/RaneemQasim5251/PathFinders/assets/108181104/107adf28-4dd8-430d-8ccc-f8eda86ce6e9)



*Animation of a simulated satellite collision (ESA, 2018).*

# Data Collection
Information about an orbiting body is encoded in a data structure called a  two-line element set (TLE) https://en.wikipedia.org/wiki/Two-line_element_set . This allows the state of an orbiting object to be accurately estimated given a time. 
The accuracy of this estimate decreases as the time deviates further away from the time at measurement, so TLE sets are regularly updated by the  North American Aerospace Defense Command (NORAD) 
https://www.norad.mil/ . 
For this project, TLE sets for various Low Earth Orbit satellites and debris were collected from Space-Track https://www.space-track.org/auth/login .

# Example TLE Set for the International Space Station
1 25544U 98067A   22114.04856634 -.00018585  00000+0 -32241-3 0  9999
2 25544  51.6451 244.7068 0005474  27.5066 137.6918 15.49633709336780

# Converting TLE to Geodetic Coordinates
Once the orbit attributes are decoded from a TLE set, further steps are required to obtain the latitude, longitude, and altitude values. There are many different models used to estimate the location of an orbiting body with a TLE set. Since this project is analyzing debris in Low Earth Orit, the  SGP4  model was used instead of SDP4, which is used for deep-space satellites.
![WhatsApp Image 2023-11-05 at 22 53 23_80cd1588](https://github.com/RaneemQasim5251/PathFinders/assets/108181104/182bfe20-e6e2-44bc-b91c-fe023e49fc2e)

# Python version:

3.9

# Python packages:
Jinja2	3.1.2 |
MarkupSafe	2.1.3 |
blinker	1.7.0 |
click	8.1.7 |
colorama	0.4.6	|
flask	3.0.0 |
importlib-metadata	6.8.0	|
itsdangerous	2.1.2	|
pip	21.1.2 |
pyproject	1.3.1 |
setuptools	57.0.0 |
werkzeug	3.0.1 |
wheel	0.36.2	|
zipp	3.17.0	

# Install packages
*Note: We used PyCharm IDE for this project*
**How do I install packages in PyCharm?**
1- Click the button on the package toolbar. <br />
2- In the Available Packages dialog that opens, preview the list of the available packages and type the name of the package to install in the Search field. <br />
3- If required, select the following checkboxes: ... <br />
4- Select the target package and click Install Package. <br />

You can also install the two main packages via pip: 

```bash
pip install flask	
```

```bash
pip install pyproject	
```

# Website URL
https://raneemqasim5251.github.io/Front-End-PathFinders-website/

# Website Video

https://github.com/RaneemQasim5251/PathFinders/assets/108181104/ef718a8a-737c-4b28-b341-fbf24e584cae


# Satellite position

https://github.com/RaneemQasim5251/PathFinders/assets/108181104/4a3fa708-e361-4b65-af2a-0729650f5c04

# Satellite movement

https://github.com/RaneemQasim5251/PathFinders/assets/108181104/e0245a78-0e30-434c-8542-d7296b94a37b


