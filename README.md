# pysdf
Python library to parse SDF into class hierarchy and export URDF

# Usage with ROS & Python
## Installation
1. Go to Catkin workspace's <code>src</code> folder (ideally located in <code>/home/\<username\>/catkin_ws/src</code>)
2. Clone this repository into the folder using: <code>git clone https://github.com/nikhilpodila/pysdf</code>
3. <code>cd ..</code> to Catkin Workspace.
4. <code>source devel/setup.bash</code>

## Running PySDF with ROS & Python
1. Open Terminal in the folder containing <code>.sdf</code> file to be converted.
2. <code>rosrun pysdf sdf2urdf.py model.sdf model.urdf</code>
3. You will get many warning messages: <code>Could not find mesh...</code><br>
This is normal. You must go to the generated <code>.urdf</code> files and change the mesh file locations to your new locations. 
Ideally, if you place your <code>.urdf</code> file in the same directory as the <code>.sdf</code> file, you can copy over all the locations between those files.
4. Verify the values in the generated <code>.urdf</code> file. You may encounter very high values in the <code>\<limit\></code> tags, which may have to be corrected.


# Usage with Python (without ROS)
## Installation and running PySDF with Python
1. Clone this repository to any convenient location.
2. Copy your <code>.sdf</code> file to the same location and open the location in cmd or Terminal.
2. <code>python sdf2urdf.py model.sdf model.urdf</code>
3. You will get many warning messages: <code>Could not find mesh...</code><br>
This is normal. You must go to the generated <code>.urdf</code> files and change the mesh file locations to your new locations. 
Ideally, if you place your <code>.urdf</code> file in the same directory as the <code>.sdf</code> file, you can copy over all the locations between those files.
4. Verify the values in the generated <code>.urdf</code> file. You may encounter very high values in the <code>\<limit\></code> tags, which may have to be corrected.

###### sources: https://roboy-ik-doc.readthedocs.io/en/latest/pysdf/
