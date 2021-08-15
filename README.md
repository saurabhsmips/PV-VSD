# PV-VSD
Physical Verification using Skywater 130nm technology

# PV-VSD
# Physical Verification using Skywater 130nm technology
This is the workshop is to understand the Skywater 130nm PDK in detail while using different open-source EDA Tools available. Also, workshop is to focus upon DRC/LVS violations during Design cycle. Each day we have Lab session to deep dive into basic concept of Physical Verification.
# @Day1

# Introduction of Skywater PDK

With the help of open source EDA tool Skywater PDK are available for enthusiastic learners.

https://github.com/google/skywater-pdk

efabless.com is helping designers to create their own design and take the project to tape out with the support of Google and Skywater.

![carvel](https://user-images.githubusercontent.com/88837856/129290885-1f09f7c5-0ccd-4622-bf5a-2b458bc471e7.png)


# Skywater Open PDK
## Documentation

https://skywater-pdk--136.org.readthedocs.build/en/136/index.html#

## PDK Libraries and files
https://github.com/google/skywater-pdk

# Open Source EDA Tools
# OpenPDK's
http://opencircuitdesign.com/open_pdks/
https://github.com/RTimothyEdwards/open_pdks

# Steps to installing the SKY130 PDK
1. Clone the repository "git clone https://github.com/RTimothyEdwards/open_pdks"
2. Run "cd open_pdks"
3. Run "configure --enable-sky130-pdk"
4. Run "make"
5. Run "sudo make install"

# Magic
http://opencircuitdesign.com/magic/
# klayout
https://klayout.de/
# Openlane
https://github.com/efabless/openlane
# Xschem
https://github.com/StefanSchippers/xschem
# netgen
http://opencircuitdesign.com/netgen/
# ngspice
http://ngspice.sourceforge.net/
# iverilog
http://iverilog.icarus.com/
# qflow
http://opencircuitdesign.com/qflow/
# irisim
http://opencircuitdesign.com/irsim/
# xcircuit
http://opencircuitdesign.com/xcircuit/

# Lab session for Day1
## Magic
<img width="960" alt="magic" src="https://user-images.githubusercontent.com/88837856/129294213-45e883fb-4623-4657-acc6-483f30364685.PNG">

# Inverter xschem
![image](https://user-images.githubusercontent.com/88837856/129464103-f1f5122d-4928-4881-b92c-98eeda82dc72.png)


![image](https://user-images.githubusercontent.com/88837856/129463348-38db5aa9-7345-4586-be8d-e5733596789a.png)

# Plot
![image](https://user-images.githubusercontent.com/88837856/129463557-9040d632-b8ec-44c6-bdbc-84a4d46b1b50.png)


# Day2 Lab

1. cif listall istyle
2. cif list istyle
3. gds read /usr/share/pdk/sky130A/libs.ref/sky130_fd_sc_hd/gds/sky130_fd_sc_hd.gds
4. cellname top
5. cif istyle sky130(vendor)
6. gds noduplicates
7. port first
8. port 1 name
9. lef read /usr/share/pdk/sky130A/libs.ref/sky130_fd_sc_hd/lef/sky130_fd_sc_hd.lef
10. load test
11. getcell sky130_fd_sc_hd__and2_1
12. gds write test
13. save test
14. load test
15. property
16. load sky130_fd_sc_hd__and2_1
17. extract all
18. ext2spice lvs
19. ext2spice
20. extresist tolerance 10
21. extresist

![image](https://user-images.githubusercontent.com/88837856/129473426-28524b7d-7c6d-482d-b216-19459e86b5fe.png)

![image](https://user-images.githubusercontent.com/88837856/129474015-a2350165-0f7b-4362-987e-2bec95934e9c.png)

![image](https://user-images.githubusercontent.com/88837856/129473855-a172acc5-c472-462e-bcaf-336cd523ffde.png)

![image](https://user-images.githubusercontent.com/88837856/129475215-c09e4653-dfff-4110-baeb-94ee7d205a17.png)

![image](https://user-images.githubusercontent.com/88837856/129475263-9230c087-c3a0-4f62-9290-d80bbf45d344.png)

![image](https://user-images.githubusercontent.com/88837856/129475475-17254dd5-d00f-431a-8165-a92b4f9fa2ce.png)

# Setup for DRC
1. /usr/share/pdk/sky130A/libs.tech/magic/run_standard_drc.py /usr/share/pdk/sky130A/libs.ref/sky130_fd_sc_hd/mag/sky130_fd_sc_hd__and2_1.mag
2. load sky130_fd_sc_hd__and2_1
3. drc style
4. drc listall style
5. drc style drc(full)
6. drc check
7. drc why
8. drc find
9. save test3

![image](https://user-images.githubusercontent.com/88837856/129475718-212583e0-932a-48f4-9a55-a5f0eedf3251.png)

![image](https://user-images.githubusercontent.com/88837856/129475757-582a90b4-e5cc-490e-b5a0-3e3c17fabf11.png)

![image](https://user-images.githubusercontent.com/88837856/129476041-7e030bfa-6452-4614-863d-e19098feca59.png)

# setup for LVS
1. mkdir netgen
2. cd netgen
3. cp /usr/share/pdk/sky130A/libs.tech/netgen/sky130A_setup.tcl ./setup.tcl
4. netgen -batch lvs " arguments"

![image](https://user-images.githubusercontent.com/88837856/129476435-f6c102e7-4d6c-45c3-8de9-279f120c7495.png)

![image](https://user-images.githubusercontent.com/88837856/129476424-07bba757-f1ba-45f6-a0ac-ee368df63fbe.png)

# setup for XOR
To compare the layout of two files
xor -nolabels xor_test


# Day3 Lab
# Width Rule and Spacing Rule

git clone https://github.com/RTimothyEdwards/vsd_lvs_lab.git

![image](https://user-images.githubusercontent.com/88837856/129479373-badfb6df-486b-4aaa-8ac8-9859400d3f51.png)

![image](https://user-images.githubusercontent.com/88837856/129480005-546edd20-2a62-4f64-877e-ae9c70256934.png)

![image](https://user-images.githubusercontent.com/88837856/129480629-4478b15f-1bc4-4922-b995-2acf242ee1ae.png)

![image](https://user-images.githubusercontent.com/88837856/129480794-8299cf44-0a43-4f1d-a08a-071b4512ce45.png)

![image](https://user-images.githubusercontent.com/88837856/129481560-f63da622-de3a-448d-a26f-2bb6ab9571f3.png)

![image](https://user-images.githubusercontent.com/88837856/129482521-5452878c-1d70-41a1-8f79-49f3ac377e20.png)

![image](https://user-images.githubusercontent.com/88837856/129486652-6ce8d493-d4d6-4577-8db2-839e3a9f0c1d.png)

![image](https://user-images.githubusercontent.com/88837856/129486730-e448fd17-b016-49a4-9b9b-b933c9392523.png)

cellname
save
property

![image](https://user-images.githubusercontent.com/88837856/129486748-221a489c-bda5-422c-8bf7-ca9b87e78259.png)




# Day4 Lab
# LVS

![image](https://user-images.githubusercontent.com/88837856/129487176-d518cbd1-18a8-438f-975d-2895d017d1f6.png)

![image](https://user-images.githubusercontent.com/88837856/129487206-13e56135-e7b9-4fb7-9f2a-fedd6640e81f.png)
![image](https://user-images.githubusercontent.com/88837856/129488026-27cab338-ddd0-4fe6-b496-f1925dada22c.png)

![image](https://user-images.githubusercontent.com/88837856/129487485-3b6694bc-70e6-4dcf-a498-0bac8526948f.png)

![image](https://user-images.githubusercontent.com/88837856/129487533-b9c5eae9-3a71-4553-a2fc-5abcc087e64e.png)
![image](https://user-images.githubusercontent.com/88837856/129487584-f9f07666-85b0-4c28-ba6b-fb0d337d6317.png)

![image](https://user-images.githubusercontent.com/88837856/129487645-a567c8f7-e852-40ac-9b35-a24531c9a3ab.png)
![image](https://user-images.githubusercontent.com/88837856/129487691-690cb654-3928-4b88-aa7a-025ae4522a85.png)


![image](https://user-images.githubusercontent.com/88837856/129487840-ef8ede66-cf33-4d24-9daa-33eeb08b6441.png)
![image](https://user-images.githubusercontent.com/88837856/129487851-30918eb6-25e4-4932-92f0-2e60d2c07853.png)
![image](https://user-images.githubusercontent.com/88837856/129487894-5db554f6-ffbf-431d-9945-7427b0156416.png)
![image](https://user-images.githubusercontent.com/88837856/129487971-9eb6100f-f901-48db-9687-e8a9ea8bf2fb.png)
![image](https://user-images.githubusercontent.com/88837856/129488029-0ad8bb8d-0f8b-461b-b5ae-78cce3c1f588.png)


![image](https://user-images.githubusercontent.com/88837856/129488218-a4b84264-df85-43fe-b0c5-206ef68512c8.png)


![image](https://user-images.githubusercontent.com/88837856/129488318-b9bdcd8c-84cf-4b07-a15f-b65a35cb3389.png)
![image](https://user-images.githubusercontent.com/88837856/129488326-7d5d92c1-7d99-4332-8b02-f6987a34545b.png)

![image](https://user-images.githubusercontent.com/88837856/129488553-e3491e91-985a-45b8-857b-77c4a3220e36.png)

![image](https://user-images.githubusercontent.com/88837856/129488671-6a5a6d39-221a-4267-9657-5a50d69cf56f.png)

