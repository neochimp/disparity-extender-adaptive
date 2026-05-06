# Modified Disparity Algorithm
 
## F1Tenth

[F1Tenth](https://roboracer.ai/) is a global racing competition where teams race autonomous cars 1/10 the scale of traditional F1 vehicles.

## Disparity Extender

This algorithm is a personal extension to the original Disparity algorithm used by a team from [UNC-Chapel Hill](https://www.nathanotterness.com/2019/04/the-disparity-extender-algorithm-and.html) who won the F1Tenth competition held at CPSWeek 2019. 

## Disparity Extender Adaptive

Our extension of the original disparity used by UNC-Chapel Hill focuses on PD-based speed control and Gaussian weighted best-angle selection in order to achieve smoother, more stable navigation. 

### PD Controller

In order to handle smaller tracks with tight turns, we adaptively scale the speed using a proportional-derivative controller to calculate a "danger" value based on clearance ahead of the car and how quickly it is approaching an obstacle. This works to improve the control the car has for making sharp maneuvers in tracks smaller than the typical racing layout.

### Gaussian weight

In order to prevent unpredictable swerving in very large maps, we apply a gaussian curve weight to the potential paths the car can take based on its distance from the center. This gives a priority to paths that keep the car aligned forward without preventing it from making sharp turns when necessary.
