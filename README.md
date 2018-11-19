# ECS-174-PS_3

1. Raw descriptor matching: Allow a user to select a region of interest (see
provided selectRegion.m) in one frame, and then match descriptors in that region to
descriptors in the second image based on Euclidean distance in SIFT space. Display the selected
region of interest in the first image (a polygon), and the matched features in the second image,
something like the below example. Use the two images and associated features in the provided
file twoFrameData.mat (in the zip file) to demonstrate. Note, no visual vocabulary should
be used for this one. Name your script raw_descriptor_matches.m

2. Visualizing the vocabulary: Build a visual vocabulary. Display example image patches
associated with two of the visual words. Choose two words that are distinct to illustrate what
the different words are capturing, and display enough patch examples so the word content is
evident (e.g., say 25 patches per word displayed). See provided helper function
getPatchFromSIFTParameters.m. Explain what you see. Name your script
visualize_vocabulary.m. Please submit your visual words in a file called kMeans.mat.
This file should contain a matrix of size kx128 called kMeans.

3. Full frame queries: After testing your code for bag-of-words visual search, choose 3
different frames from the entire video dataset to serve as queries. Display each query frame
and its M=5 most similar frames (in rank order) based on the normalized scalar product
between their bag of words histograms. Explain the results. Name your script
full_frame_queries.m

4. Region queries: Select your favorite query regions from within 4 frames (which may be
different than those used above) to demonstrate the retrieved frames when only a portion of the
SIFT descriptors are used to form a bag of words. Try to include example(s) where the
same object is found in the most similar M frames but amidst different objects or
backgrounds, and also include a failure case. Display each query region (marked in the
frame as a polygon) and its M=5 most similar frames. Explain the results, including possible
reasons for the failure cases. Name your script region_queries.m

5. Full frame queries, Part 2: comparing SIFT bag-of-words with Deep Features:
Use frames friends_0000004503.jpeg and friends_0000000394.jpeg to serve as
queries. For each query display: the query frame and (1) its M=10 most similar frames based on
the normalized scalar product between their bag of words histograms and (2) its M=10 most
similar frames based on the normalized scalar product between their AlexNet fully-connected
layer 7 activation features (stored as variable deepFC7). (The AlexNet was pre-trained on the
1000-class ImageNet classification task, and we are using it to extract the layer-7 activation
features for each image.) Explain the differences between the retrieval results obtained using the
SIFT bag-of-words features versus the pre-trained deep convolutional neural network features.
Which does better? Why? Name your script compare_bow_and_deep.m
