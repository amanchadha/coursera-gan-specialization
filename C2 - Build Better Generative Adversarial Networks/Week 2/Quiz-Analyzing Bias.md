# Quiz: Analyzing Bias
1. One measure of fairness is demographic parity, which means that the positive percentage is the same for all groups. Suppose Ants are 60% of the population, and Bunnies are 40% of the population. Your model predicts a positive result for 10 Bunnies. For how many Ants should the model predict a positive result to satisfy demographic parity?
- [x] **15**
- [ ] 8
- [ ] 10
- [ ] Cannot be determined

2. One measure of fairness is equality of odds, which means that, all else being equal, the model is equally likely to make a positive prediction for a member of either class. Suppose that being able to run fast is meaningful to the prediction, and other properties are not considered. Your model predicts a positive result for 3 of the 30 Cats which can’t run fast, and 20 of the 40 Cats which can run fast. If there are 10 Dogs which can’t run fast, and 20 which can run fast, how many positive predictions should there be for equality of odds?
- [x] **11**
- [ ] 15
- [ ] 14
- [ ] 3

3.Another measure of fairness is equal opportunity, which means that those members with a property should have equal probability of a positive prediction, but not necessarily those without that property. Suppose that the ability to fly is meaningful to the prediction, and other properties are not considered. Your model predicts a positive result for 10 of the 80 Elephants which can’t fly, and 15 of the 20 Elephants which can fly. If there are 40 Flamingos which can’t fly and 60 which can fly, which of these are valid numbers of positive predictions under equal opportunity:
- [x] **40 flightless Flamingos, 45 flying Flamingos**
- [ ] 12 flightless Flamingos, 13 flying Flamingos
- [ ] 10 flightless Flamingos, 20 flying Flamingos
- [ ] 0 flightless Flamingos, 50 flying Flamingos

4. One measure of fairness is “fairness through unawareness” which suggests that a model is fair if the protected attribute differentiating Class A and Class B is not given to the model. Which of the following are you able to assume?
- [ ] The model will give roughly the same predictions for members of Class A and Class B.
- [ ] At least one of equal opportunity, equality of odds, or demographic parity must be satisfied.
- [ ] The model would change its predictions if explicitly given the protected attribute — i.e. the attribute is not implicit in the input data.
- [x] **None of the above.**

5. Suppose that your friend implemented a standard DCGAN on a dataset they compiled and manually labeled 1,000 generator outputs for some feature which they care about. Your friend then changes their generator to also output the nearest label in z-space (by Euclidean distance) whenever it generates an image. What are some potential sources of bias here?
- [x] **Since your friend single-handedly labeled the images, it is possibly they introduced some of their own bias to the model.**
- [x] **Since the generated images are sampled images from a Gaussian distribution, the use of Euclidean distance is likely to bias the label output with respect to distance from the center of the distribution**
- [x] **It cannot be assumed that their method of compilation was representative.**
- [ ] None of the above.


6. Your friend tells you that they have a conditional GAN, where they added an extra loss to the generator to encourage it to reproduce the ground truth image given the conditions. They do this by penalizing the distance from the generated image to the original image and are asking you about fairness.
Your friend wants to know whether they should use the absolute value of the pixel differences between the two images as the penalty, or the square of the differences. Images of one group of people, which are a smaller fraction of the dataset, have an average pixel brightness of 0.3 while the images of the other group have an average pixel brightness of 0.9. What are some reasonable answers you could give your friend?

- [x] **Try both and then ask impartial people from both groups to evaluate it.**
- [ ] Don’t worry about it since algorithmic decisions don’t cause bias.
- [x] **Using the quadratic (L2) loss would penalize the model more for the lighter group, so using L1 distance will likely correct for some of the dataset inequality.**
- [ ] None of the above.





