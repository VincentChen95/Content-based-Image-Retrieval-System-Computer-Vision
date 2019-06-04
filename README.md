# Content-based-Image-Retrieval-System-Computer-Vision
<br> I developed a content-based image retrieval system that retrieves database images based on the similarity between their regions and those of a query image.In this task, I used 20 features, including 'contrast', 'entropy', 'homogeneity', 'energy', '(min_x+max_x)/(2*w)', '(min_y+max_y)/(2*h)', 'max_x/w', 'max_y/h', 'min_x/w', 'min_y/h', 'centroid column/(w*count)', 'centroid row/(h*count)', 'region pixel count[i]/(w*h)', '(max_x - min_x)/w'. '(max_y - min_y)/h', and '(max_y - min_y)*(max_x - min_x)/(w*h)'.
<br> max_y, min_y, max_x, and min_x are the co-ordinates of the corners of bounding box of each region.
<br> I chose these features from two aspects. One from color, another one from bounding box. 'contrast', 'entropy', 'homogeneity', 'energy', these four are related with co-occurrence text features.
<br> Size and mean color in RGB color space, these four features are provided by default. Centroid feature including centroid column and centroid row features.
<br> I used the co-ordinates of four corners of the bounding box to calculate nine ratio features. Moreover, I used the ration of count of pixels in each region as a feature. The final result shows that these features work very well.
<br> Meanwhile, I used the 'Euclidean distance' ((v_{pi}-v_{qi})^{2})^{0.5} and the 'Squared Chord Distance' (v_{pi}^{0.5}-v_{qi}^{0.5})^2 to calculate the distance of feature. I also tried 'Canberra Distance'. The 'Squared Chord Distance' and 'Euclidean distance' work better, so I chosen 'Squared Chord Distance'. According to the average accuracy, the 'Euclidean distance' works better than the 'Squared Chord Distance'. In the feature space, the 'Euclidean distance' may capture more space information than 'Squared Chord Distance'.
## Retrieval Result
![beach_1_1](https://user-images.githubusercontent.com/36937088/58913325-cea8cf80-86d0-11e9-8bab-4dd23f35cb59.png)
![cherry_3_1](https://user-images.githubusercontent.com/36937088/58913342-d6687400-86d0-11e9-8620-9eb8774b0b2b.png)
![sunset_1_1](https://user-images.githubusercontent.com/36937088/58913352-dbc5be80-86d0-11e9-9fdc-a9c410b5f50b.png)
