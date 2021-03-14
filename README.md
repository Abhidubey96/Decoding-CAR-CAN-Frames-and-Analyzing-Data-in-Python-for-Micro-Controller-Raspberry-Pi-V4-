# Decoding-CAR-CAN-Frames-and-Analyzing-Data-in-Python-for-Micro-Controller-Raspberry-Pi-V4-
Decoding CAR CAN Frames and Analyzing Data in Python for Micro Controller (Raspberry Pi V4)


Python Notebook: Abhishek Dubey
Contact: abhishekdubey.irl@gmail.com
Problem:
work is mainly based on Vehicle data (Cars) we analyse all possible raw information we can get to achieve knowledge and insights on the situation.

One of the sources of data is generated from the CAN-ODB port of the Car. This port gives information about the Car such as the engine speed, the torque, fuel consumption, etc. The port is extremely sensitive and will provide data at approx. 20-25 Frames per second. These frames are called CAN frames, where each frame consists of the Timestamp, hexadecimal ID, and a Hexadecimal message. “CAN_log.asc” file is a log file with all the CAN frames for a car.

The hexadecimal message is decoded to get the variables and their values at that timestamp like engine speed, torque, etc. To decode these frames, you need a “.dbc” file it is called a CAN database file. The file describes the meaning and format of decoding the hexadecimal messages using the hexadecimal IDs in the frame. Let us consider the following frame as an example:

Here 208 is the hexadecimal ID and 1F 45 3E 0B 4C 3E 32 3F is the hexadecimal message.

The above snippet is from “CAN.dbc”, here the ID 520 is the decimal id for the hexadecimal id 208. Below the ID is the description of how the hexadecimal message will be decoded to find the corresponding variables. The variables are in French so Regime_moteur is engine speed.

Your Task is to:
1) Decode only frames with ID 208 and extract only the values for variable “Regime_moteur”. Retain the corresponding timestamp as well. 2) Then create an interactive plot where: 3) y axis is Regime_moteur – The values are normalised using min-max normalization min=0 and max = 5000 4) x axis is the timestamp – Format “HH:MM: SS”. 5) Then store it in the form of an output video/gif

Solution:
Python 3.9.1
Import Libraries

Cantools for Can files

Matplotlib for plotting graph and animation

pandas for working in data frames

numpy for creating array for value insertation

print for pillow and printing image

For more please check Python Notebook File

Thanks :)
