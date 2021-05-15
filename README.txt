Problem:
A wire through which a current is flowing lies along the x-axis as shown. Connecting wires which are not shown in the diagram connect the ends of the wire batteries (which are also not shown). Electron current flows through the wire in -x direction, as indicated in the diagram. To calculate the magnetic field at location A due to the current in the wire, we divide the wire into pieces, approximate each piece as a point charge moving in the direction of conventional current, and calculate the magnetic field at the observation location due only to this piece; then add the contributions of all pieces to get the net magnetic field. The wire is 1.3 m long and is divided into 8 pieces. The observation location A is located at < 0.081, 0.178, 0> m. The conventional current running through the wire is 7.1 amperes. Calculate the net magnetic field at location A due to the wire. 

Purpose and Use:

The purpose of the code is to caluclate the net magnetic field at 
location A due to the wire using the biot-savart law. The wire 
can be split into 8 segments. The current in each segment of the wire contributes
to the net magneitc field at location A. The center of the each segment can be
used to approximate the magnetic field at location A. 

Biot Savart Law:

dB = ((I*mu_0)/4*pi)*((dl cross r_hat)/|r|^2)

I = Current in Amperes. 
mu_0 = magnetic constant.
d1 = vector that describes the length of segment. It is in the direction of 
     conventional current.
r = vector from the location of a segment of wire (center of the segment)
    to the location of interest (in meters). 
r_hat = unit vector of r vector

Since there are 8 segments, the magneitc field due to each segment at location A
must be calculated.

Therefore, 

dB_net = dB_1 + dB_2 + dB_3  + dB_4  + dB_5  + dB_6  + dB_7  + dB_8 

The code was written in such a way that the net magnetic field at any
location due to the wire in the question can be calculated. The current of the 
wire can also be manipulated.

Thus, the primary inputs are A (location of interest) and I (current in wire). 
________________________

# Given information:

	Here all important variables given from the problem are assigned.

# Segment Calculations:
	
	Here all the initial and final locations of each segment is determined
	in reference to a coordinate system where the center of the wire is the origin.

# Centers and dl vectors:
	
	Here all the dl vectors for each segment is determined using the intial and final
	locations of each segment. The center of each segment is determined to calculate
	the r vector and r_hat in the next section. 

# Calculate r_vec and r_hat:

	r_hat and r vector is calculated for each segment.

# Calculate dl cross r_hat:

	Cross product of each dl vector and r vector is determined.

# Calculate the magnetic field at observation location: 
	
	Here the dB due to each segment is determined. 

# Net Magnetic field at location A:

	Here the net magneitc field is determined by taking the sum of db_1:dB_8.

# Print:

	Here the magnetic field due to each segment at A is printed. The net magetic field at A is also printed. 
