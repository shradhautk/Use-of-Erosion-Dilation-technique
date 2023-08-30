# Use-of-Erosion-Dilation-technique
Investigating the Impact of Post-processing Techniques like Erosion and Dilation on the Performance of Models Utilizing Various Loss Functions, including Binary Cross-Entropy, Weighted Binary Cross-Entropy, Distance, Dice, and IOU.

The primary objective of this experiment is to compare and evaluate the performance of various loss functions in the context of semantic segmentation of helium cavities in electron microscopy images. Specifically, we aim to identify the most effective loss function for accurately segmenting these radiation-induced defects, which play a crucial role in determining the swelling value of nuclear materials. By assessing different loss functions, including Dice, Cross-entropy, Weighted Binary Cross Entropy (WBCE), and Intersection over Union (IOU), we seek to identify the optimal approach to enhance the precision and reliability of the segmentation process, ultimately contributing to the safe operation of nuclear reactors and materials.

These 5 codes could be used to do the post-processing of p-maps. In our case, it did not improve the precision and recall to a large extent. We used a circular kernel of diameter 5 for opening (i.e. erosion followed by dilation). Please see the results below:


Old value (obtained without post-processing techniques such as erosion and dilation):
Loss functions	Precision	Recall	Accuracy	IOU	Mean Absolute Area Error
IOU	0.843230	0.873784	0.9515032	0.752194	0.0854534
Dice	0.864738	0.882732	0.95773683	0.775554	0.0766843
WBCE	0.805468	0.9258342	0.9506608	0.756746	0.1572016
BCE	0.871443	0.8637240	0.9563726	0.766329	0.06279365
Distance	0.881000	0.8502019	0.9563932	0.762580	0.07180912




New value (obtained with post-processing techniques such as erosion and dilation): 
Loss functions	Precision	Recall	Accuracy	IOU	Mean Absolute Area Error
IOU	0.843718	0.873417	0.951559	0.752	0.085057
Dice	0.864737	0.882733	0.957737	0.775554	0.076686
WBCE	0.807454	0.924751	0.951034	0.757	0.153211
BCE	0.871443	0.863723	0.956373	0.766329	0.062793
Distance	0.882664	0.84819	0.956418	0.762207	0.072

 

