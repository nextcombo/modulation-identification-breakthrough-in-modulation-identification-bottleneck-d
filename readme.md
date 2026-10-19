# [Modulation Identification] Breakthrough in Modulation Identification Bottleneck: Deep Convolutional Neural Network Solution Based on Multi-task Learning, Accuracy Increases by 5%! [Attached Python Code]

The core characteristic of cognitive radio is situation awareness. By classifying the modulation methods of signals transmitted around, secondary users (SU) can identify existing users in the system and adjust their transmission parameters accordingly. This paper proposes a deep convolutional neural network (CNN) method based on multi-task learning (MTL) for recognizing specific sets of analog and digital modulation methods. The method trains individual classifiers for confusing modulation categories through multi-task learning to reduce classification confusion and improve overall accuracy. Experimental results on the RadioML dataset show that compared to the recently proposed Convolutional-Long Short-Term Memory-Deep Neural Network (CLDNN), this architecture achieves higher overall classification accuracy: 86.97% at a 18 dB signal-to-noise ratio (SNR), an improvement of 5% over existing technology.
Introduction With the explosive growth of wireless data demands, improving the efficiency of spectrum allocation has become key. Cognitive radio (CR) technology emerged, which can identify primary users (PU) through spectrum perception and adjust its parameters to avoid interference by identifying modulation methods. Identifying the modulation type of surrounding signals is the core link in achieving this goal — accurate recognition of the modulation types allows CR to truly possess "situation awareness."
However, similarities between different modulation methods often lead to classification confusion. For example, QPSK in digital modulation and 8PSK, QAM16 and QAM64, as well as AM-DSB and WBFM in analog modulation, due to their similar features, are difficult for traditional methods to distinguish. In recent years, machine learning, especially deep learning (such as convolutional neural networks CNN), has shown potential in modulation recognition, but existing models are still limited by such confusion issues.
This paper proposes a multi-task learning convolutional neural network (MTL-CNN) to specifically solve the problem of recognizing confusing categories, improving overall performance by separating training critical tasks, providing a new solution for efficient spectrum utilization in cognitive radio.
In the article, illustrations illustrate the core idea
Multi-task learning (MTL) is a core approach that involves training multiple related tasks in parallel, leveraging the interrelationships between them to enhance the model's ability to learn key features. In modulation recognition, MTL-CNN decomposes the overall classification task into three key subtasks (for ambiguous categories) and one main classification task:
Subtask 1: Distinguishing QPSK from 8PSK (Digital Modulation);
Subtask 2: Distinguishing QAM16 from QAM64 (Digital Modulation);
Subtask 3: Distinguishing AM-DSB from WBFM (Analog Modulation);
Main Task: Final classification for all ten modulation types.
Network Architecture
Input layer: For digital modulation, utilizes the frequency domain feature of the signal (FFT result), and for analog modulation, uses the raw I/Q signal (time domain feature), fully utilizing the differences in features from different domains;
Feature extraction: Through two convolutional layers to extract key features, the first layer contains 128 1×3 filters, and the second layer contains 80 2×3 filters;
Multi-task fusion: The outputs of the subtasks are fused through shared layers, then passed through fully connected layers and SoftMax to output the final classification results, balancing the details of the subtasks with the global classification of the main task.
Advantages
Compared to traditional CNN and CLDNN, MTL-CNN reduces misclassification caused by feature similarity by specifically training ambiguous categories, while combining the differentiation design of frequency and time domain inputs provides the model with richer feature information.
Conclusion: Experimental results show that on the RadioML dataset (containing 10 modulation types and 1.2 million samples), MTL-CNN significantly outperforms existing models:
Overall classification accuracy reaches 59.44% (over all SNR range), higher than CLDNN's 58.37% and traditional CNN's 57.39%;
Under a 18 dB high signal-to-noise ratio, the accuracy soars to 86.97%, an improvement of 5% over existing technology, and completely eliminates confusion between QPSK and 8PSK, significantly reducing the misjudgment rate for QAM16/QAM64, AM-DSB/WBFM.
This achievement provides a more efficient solution for modulation identification in cognitive radio. Future expansion to more modulation types can be further realized, combined with Software Defined Radio (SDR) for real-time scenario verification, promoting the application of cognitive radio in complex spectrum environments.
End

## Images

![(Modulation Identification)Breakthrough in Modulation Identification Bottleneck: Deep Convolutional Neural Network Solution Based on Multi-task Learning, Accuracy Increase by 5%! [Python Code Included]](01.jpg)
![(Modulation Identification)Breakthrough in Modulation Identification Bottleneck: Deep Convolutional Neural Network Solution Based on Multi-task Learning, Accuracy Increase by 5%! [Python Code Included]](02.jpg)
![(Modulation Identification)Breakthrough in Modulation Identification Bottleneck: Deep Convolutional Neural Network Solution Based on Multi-task Learning, Accuracy Increase by 5%! [Python Code Included]](03.jpg)
![(Modulation Identification)Breakthrough in Modulation Identification Bottleneck: Deep Convolutional Neural Network Solution Based on Multi-task Learning, Accuracy Increase by 5%! [Python Code Included]](04.jpg)
![(Modulation Identification)Breakthrough in Modulation Identification Bottleneck: Deep Convolutional Neural Network Solution Based on Multi-task Learning, Accuracy Increase by 5%! [Python Code Included]](05.jpg)
![(Modulation Identification)Breakthrough in Modulation Identification Bottleneck: Deep Convolutional Neural Network Solution Based on Multi-task Learning, Accuracy Increase by 5%! [Python Code Included]](06.jpg)

<!-- PAYMENT_BLOCK -->

## Get this dataset

- Payment link (Stripe): [Buy now](https://buy.stripe.com/3cs8yP7sY87d0vu9AB)
- Payment QR code: ![Payment QR code](pay.png)

<!-- /PAYMENT_BLOCK -->
