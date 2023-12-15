# OSS_TEST  
**Detect Crosswalk, Object(Human, Car)**  
Find objects in the image(jpg) and mark them as boxes.

## Source code setting
Two ways path setup:  
	i. Image and source code in the same folder  
	``` python detect_crosswalk_human_car('walk_people.jpg')
	```  
	ii. A folder whatever named with source code and an image folder  
	``` python detect_crosswalk_human_car('./image/walk_people.jpg')  
	```  
## Steps involved:
Install python, opencv, numpy  
Download text file  
Read image  
Create red color mask  
Find contours for crosswalk detection  
If crosswalks are found, draw bounding box around them  
For each detected object  
Merge the boxes human and car

## Demo Image
<img src="/path/to/walk_people.jpg" width="40%" height="30%" title="px(픽셀) 크기 설정" alt="RubberDuck"></img>
## Used (version, YOLO text file, image size)
1. python (3.12.0)  
2. opencv(4.8.1.78)  
3. numpy (1.26.2)  
4. Image (1080 x 720)  
***Python  
https://www.python.org/downloads/  
Yolo  
https://github.com/pjreddie/darknet/blob/master/cfg/yolov3.cfg
https://github.com/pjreddie/darknet/blob/master/data/coco.names***

## Image Source
Link: [Freepik](https://kr.freepik.com/free-photo/stylish-young-couple-posing-outdoors-a-young-man-with-a-bristle-in-a-cap-with-a-girl-with-long-hair-happy-young-people-are-walking-around-the-city-portrait-close-up_1210198.htm#page=3&query=%EA%B1%B0%EB%A6%AC%EB%A5%BC%20%EA%B1%B7%EB%8A%94%20%EC%82%AC%EB%9E%8C%EB%93%A4&position=25&from_view=keyword&track=ais&uuid=d327b96e-8d01-4496-9e12-678e18186db2)  
<a href="https://kr.freepik.com/free-photo/stylish-young-couple-posing-outdoors-a-young-man-with-a-bristle-in-a-cap-with-a-girl-with-long-hair-happy-young-people-are-walking-around-the-city-portrait-close-up_1210198.htm#page=3&query=%EA%B1%B0%EB%A6%AC%EB%A5%BC%20%EA%B1%B7%EB%8A%94%20%EC%82%AC%EB%9E%8C%EB%93%A4&position=25&from_view=keyword&track=ais&uuid=d327b96e-8d01-4496-9e12-678e18186db2">작가 Kireyonok_Yuliya</a> Source Freepik
