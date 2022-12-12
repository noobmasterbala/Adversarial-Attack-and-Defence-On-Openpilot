# Adversarial_Attack_and_Defence_On_Openpilot

OpenPilot is an open-source driver assistance system that uses computer vision and machine learning algorithms to provide advanced features, such as lane keeping and adaptive cruise control, in vehicles. The software is designed to be installed on compatible vehicles, where it can process data from the vehicle's cameras and sensors to provide advanced driver assistance features. OpenPilot is intended to be a flexible and extensible platform that allows users to customize and enhance its capabilities, and to contribute back to the community.

In this project we have performed whitebox attack on the openpilot model. 
In a white box attack, the attacker has access to the system's internal structure, algorithms, data, and network architecture, and can use this information to craft more sophisticated and targeted attacks. White box attacks are often used to evaluate the security of a system, and can provide valuable insights into potential vulnerabilities and weaknesses. They are typically more difficult to defend against than black box attacks, in which the attacker has no knowledge of the system's internal workings.

# Attack

We have performed the adversarial patch attack on the openpilot model. The video data from the Autonomous Vehicle's (AV) camera is decomposed into frames. Then the adversarial patch attack is performed on some frames. An adversarial patch attack on is a type of security attack in which the attacker creates a small patch or region of an image that is specifically designed to mislead or confuse an image recognition system. The patch is typically generated using machine learning algorithms that are trained to generate patches that are difficult to detect, but that have a significant impact on the outcome of the image recognition process. Adversarial patch attacks are often used to evaluate the robustness and vulnerability of image recognition systems, and can provide valuable insights into potential weaknesses and areas for improvement. 



# Defense 
In mathematics, the Fourier transform is a mathematical operation that decomposes a function into its constituent frequencies. This is useful in many fields, including signal processing, image processing, and data analysis, because it allows complex, time-varying signals to be represented in a more manageable and interpretable form. 

Fourier transform can be used to analyze and defend against adversarial attacks on the frames from our data. Our approach is to apply the Fourier transform to the frames, and then analyze the frequency components of the resulting representation to identify potential adversarial perturbations. This can be done by comparing the frequency spectrum of the original image to that of the perturbed image. We have trained a Random Forest Classifier to classify between original and adversarial frames. Once an adversarial frame has been detected we reject these manipulated frames. 
