# AutoML for American Sign Language classification

TGIF project: a day using AutoML to classify ASL images

Please click the video to hear sound or follow along with the transcript / slides below the video.     
(In this case, the video integrates several illustrations and is better than a set of transcript & slides could present.)   

![demo](https://user-images.githubusercontent.com/38410965/111720421-3394d180-8834-11eb-8674-59f37f840aac.mp4)

#

**Steve Depp 
MSDS 462 
Section 55 
Demo Video 4** 

**American Sign Language dataset**

> Hello. These are the images of the American Sign Language data set. 

<img width="435" alt="image" src="https://user-images.githubusercontent.com/38410965/116020809-05fe2d80-a615-11eb-8de1-d8939512d794.png">

#

> There are 3000 samples for each of 26 letters.  I had wanted to work with these larger full color images last year, but the 400,000 pixels and 3 colors prevented quick modeling.  Google's AutoML essentially mastered the task with a nearly a perfect F1 score for confidence levels between ~7 and 80%.   

**American Sign Language dataset**

| samples      | 3,000          |
| ------------ |:-------------- |
| classes      | 26 + 1 + 1     |
| information  | 200 x 200 x 3  |

samples		3000 
classes		26 + 1 + 1 
information	200 x 200 x 3

[2nd slide- 4thslide]

You can also see they made the process very convenient by emailing me ...

... when the data set was loaded which took a few minutes, 

... when model had finished training which took about 4 hours, 

... and when the trained model had deployed for inference. 

[5thd slide. EVAL]
[GCP evaluation screen]
[finder]

Another key benefit of Auto ML is that performance comes with excellent interactive visualization.  Since most executives learn via interacting, this is a huge plus.  

For example here’s are 3 instances of interacting with the Evaluation tab.  

I can slide this confidence bar from 50% where F1 is 1 to 80% where recall falls below 100%.

Maybe in a negotiation or science presentation or doctor's visit, this would be appropriate. 

If I slide it further to 7% confidence, precision suffers but only to about 97%.

This result might justify using a one shot only model where confidence is low, but speed is high like in a crowded restaurant.

[finder Scroll through images]

Best I can tell, the images are stills lifted from video.

Here is a sequence of young person with pale skin hand signing the letter "A" in a uniform background through shade and sunlight for better generalization.

This model wouldn’t for example generalize very well for dark skinned, thicker and older individual in a dark restaurant. 

[NExt slide DATA]

The total size of the dataset is just under a gig uncompressed.  

Doing the math on three thousand 3-bit images with 400,000 pixels, I couldn’t arrive at the same number so I explored a bit.   

[Fourth slide]

One result is finding that darker images, here on the bottom, tend to have less information.

Here, you can see the lighter image with 15,000 bytes has more edges than the darker file with only 10.000 bytes.

[FIINDER can show resorting images]

A one gigabyte of image import too large for AutoML. 

Google cloud bucket with CSV conversion is too cumbersome. 

Selecting 200 images in alphabetic order was not an option because, as you can see, they are highly correlated .

As a hack, I sorted by size instead of by name and selected only the 200 smallest images.  So, for example, go down here, change this to size, and now you pick sequential images, they're very different.  

Only later did I consider that I was using the smallest sized images in the sorting scheme.

[LAST sslide ]
[test pane on GCP

Testing is a snap which illustrates the power of visualization.

For the letters "A" through "G", performance was mostly spot on.
The last 7 letters did not do so well probably because it's missing the left hand side of the hand, as in here, or the bottom of wrist, here, or again the left hand side of the hand, here. 

I do appreciate you taking the time to watch my video.  

Thank you very much. 
