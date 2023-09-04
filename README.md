# Adversarial Attack and Defense on OpenPilot

![OpenPilot Logo](open.png)

**Adversarial_Attack_and_Defence_On_Openpilot** is a research project that explores the vulnerabilities and defenses of the OpenPilot open-source driver assistance system. OpenPilot utilizes computer vision and machine learning algorithms to provide advanced features like lane keeping and adaptive cruise control in vehicles. This project focuses on whitebox attacks, specifically adversarial patch attacks, on the OpenPilot model, and proposes a defense mechanism using Fourier transform and machine learning.

## Table of Contents

- [Introduction](#introduction)
- [Attack](#attack)
- [Defense](#defense)

## Introduction

OpenPilot is a versatile and extensible platform designed to enhance driver assistance features in vehicles. It leverages computer vision and machine learning to provide advanced capabilities, and it encourages customization and community contributions. This project delves into the security aspects of OpenPilot, focusing on whitebox attacks and defense mechanisms.

## Attack

In this project, we perform a whitebox attack on the OpenPilot model. Whitebox attacks involve having access to the internal structure, algorithms, data, and network architecture of the system, enabling the crafting of sophisticated and targeted attacks. We specifically execute an adversarial patch attack on OpenPilot.

An adversarial patch attack involves manipulating frames from the Autonomous Vehicle's (AV) camera. The attacker creates a small patch or region of an image designed to mislead or confuse the image recognition system. Machine learning algorithms are used to generate patches that are difficult to detect but significantly impact the image recognition process. These attacks assess the robustness and vulnerabilities of image recognition systems.

## Defense

To defend against adversarial attacks, we employ the Fourier transform, a mathematical operation used to decompose a function into its constituent frequencies. We apply the Fourier transform to frames from our data and analyze the frequency components to identify potential adversarial perturbations. This is done by comparing the frequency spectrum of the original image to that of the perturbed image.

We train a Random Forest Classifier to differentiate between original and adversarial frames. When an adversarial frame is detected, it is rejected. In the notebook ML_Sec_Defense.ipynb, we convert adversarial and benign video frame data into a two-dimensional array of frequency coefficients using Fourier Transform. The coefficients represent the amplitude and phase of each frequency component, enabling us to analyze and manipulate the image effectively. Our Random Forest model achieves a high accuracy of 99.2% in detecting adversarial images.

