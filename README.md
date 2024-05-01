# DA623_200104036
OFDM simulation (Concept of orthogonality, and its usefulness in modeling real-world signals)

OFDM Simulation

Introduction
This project demonstrates an example of Orthogonal Frequency Division Multiplexing (OFDM), a technique used in wireless communication systems.

Overview
OFDM is a widely used modulation technique in wireless communication systems due to its robustness against multipath fading and its ability to handle high data rates. This repository provides Python code demonstrating key OFDM signal processing steps, including channel estimation, equalization, demapping, and bit error rate calculation.

Usage
1.Clone this repository to your local machine.
2.Navigate to the project directory in your terminal.
3.Run the main Python script

How it works :-

1.Initialization:
Parameters such as the number of subcarriers, pilot carriers, and modulation scheme are defined to set up the OFDM system.
2.Generating Data:
Random binary data is generated to represent the information to be transmitted.
This binary data is then mapped to complex symbols using a predefined mapping table, which assigns specific complex values to each combination of binary bits.
3.Channel Modeling:
A wireless channel is simulated using a known impulse response.
This models the effects of the wireless medium on the transmitted signal, such as multipath propagation and fading.
4.Transmission:
The complex symbols generated earlier are transformed into time-domain OFDM symbols using an Inverse Fast Fourier Transform (IFFT).
A cyclic prefix is added to each OFDM symbol to guard against intersymbol interference caused by the channel.
5.Reception:
The transmitted OFDM signal undergoes reception simulation, which includes the addition of noise to simulate real-world channel conditions.
The cyclic prefix is removed from the received signal to retrieve the original OFDM symbols.
6.Channel Estimation:
Pilot symbols embedded within the transmitted signal are used to estimate the channel response.
By comparing the received pilot symbols to their known values, the receiver can estimate the channel's characteristics, such as amplitude and phase, across different subcarriers.
7.Equalization:
The estimated channel response is used to compensate for the effects of the channel on the received signal.
This equalization process involves dividing the received symbols by the estimated channel response to recover the original transmitted symbols as accurately as possible.
8.Demodulation:
The received symbols, which have been equalized, are demapped back to binary data.
This involves reversing the mapping process performed during data generation, converting the complex symbols back into binary bits.
By following these steps, the OFDM system effectively transmits and receives data over a wireless channel, demonstrating the principles of OFDM communication.


Orthogonality plays a crucial role in the Orthogonal Frequency Division Multiplexing (OFDM) technique showcased in this project. Here's how orthogonality is utilized:
1.Subcarrier Orthogonality:
In OFDM, data is divided into multiple subcarriers, each transmitting its own unique signal.
These subcarriers are carefully spaced apart so that they are orthogonal to each other.
Orthogonality ensures that the signals transmitted on different subcarriers do not interfere with each other, allowing for simultaneous transmission without distortion.
2.IFFT and FFT Operations:
OFDM utilizes Inverse Fast Fourier Transform (IFFT) to convert digital data into time-domain OFDM symbols for transmission.
The IFFT operation ensures that the subcarriers remain orthogonal in the time domain.
At the receiver, Fast Fourier Transform (FFT) is used to convert the received time-domain OFDM symbols back into the frequency domain for demodulation.
The orthogonality property of FFT ensures that the original subcarriers can be accurately recovered without interference from other subcarriers.
3.Channel Estimation:
Pilot signals are embedded within the OFDM symbols to estimate the channel response between the transmitter and receiver.
The orthogonality of the pilot signals allows for accurate estimation of the channel response for each subcarrier.
By exploiting orthogonality, the receiver can separate the channel response of each subcarrier, enabling effective equalization and demodulation.
4.Equalization:
Channel equalization is performed by dividing the received signal by the estimated channel response.
Orthogonality ensures that the equalization process can be performed independently for each subcarrier without interference from adjacent subcarriers.
This helps mitigate the effects of channel distortion and noise, improving the overall reliability of data transmission.
In summary, orthogonality enables OFDM to efficiently divide and transmit data across multiple subcarriers while minimizing interference, thereby enhancing the reliability and performance of wireless communication systems.

Interpretation:-
Demapping and Bit Error Rate Calculation: After equalization, the received symbols are demapped back to bit groups. Subsequently, the bit error rate (BER) is calculated by comparing the transmitted bits with the received bits. The BER quantifies the accuracy of the communication system by indicating the ratio of incorrectly received bits to the total number of transmitted bits.


