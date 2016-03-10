#include <stdio.h>
#include <opencv2/opencv.hpp>

using namespace cv;

int main(int argc, char** argv )
{
    
    VideoCapture cap(0);
    if(!cap.isOpened()){
      return -1;
    } 
    
    namedWindow("Black Beads", WINDOW_AUTOSIZE );
    for(;;)
    {
        Mat frame;
        cap >> frame; // get a new frame from camera
        cvtColor(frame, frame, CV_BGR2GRAY); // convert color image to gray image
        threshold(frame, frame, 150, 255, THRESH_BINARY); // segmentation
        imshow("Black Beads", frame);
        if(waitKey(30) >= 0) break;
    }
    
    waitKey(0);

    return 0;
}