# Beginner Physical design using open-source EDA Tools
## Contents:
1. Study and review various components of RISC-V based picoSoC
2. Chip planning strategies and introduction to foundry library cells
3. Design and characterize one library cell using Magic Layout tool and ngspice
4. Pre-layout timing analysis and importance of good clock tree
5. Final steps for RTL2GDS

### The open source tools that are involved in this workshop are as follows

Yosys – for Synthesis, 
Graywolf – for Placement, 
Qrouter – for Routing, 
Netgen – for LVS, 
Magic – for Layout and Floorplanning, 
Qflow – RTL2GDS integration, 
OpenSTA & Opentimer -Pre-layout and Post-layout Static timing analysis

##DAY 1

1.Click on VSD IAT, Go to "Lab Instances". Then under "Links", click on the "link" icon. Click bottom left, System tools > LXTerminal. 2.Now type the command "yosys". What do you see next?

D1SK4 - MCQ5
*git clone https://github.com/kunalg123/vsdflow.git*
D1SK4 - MCQ6
*cd vsdflow
./vsdflow spi_slave_design_details.csv
ls -ltr outdir_spi_slave/*
![2021-03-04 (2)__01](https://user-images.githubusercontent.com/71768466/110245092-e25d2600-7f87-11eb-96e2-213f538528ac.png)
*ls -ltr outdir_spi_slave | wc*
![2021-03-04 (3)__01](https://user-images.githubusercontent.com/71768466/110245096-e6894380-7f87-11eb-9c6c-d2400af7f24e.png)
*cd outdir_spi_slave
qflow display spi_slave*
![2021-03-04 (4)__01](https://user-images.githubusercontent.com/71768466/110245099-e9843400-7f87-11eb-92ee-1bff620c3945.png)

D1SK4 - MCQ8
*cd
cd vsdflow
mkdir my_picorv32
cd my_picorv32
mkdir source synthesis layout
cp ~/vsdflow/verilog/picorv32.v source/.
qflow gui &*
Select below options in gui

Technology = osu018
Verilog source file : picorv32.v
Verilog module : picorv32
Click on Set Stop
![2021-03-04 (5)__01](https://user-images.githubusercontent.com/71768466/110245103-ebe68e00-7f87-11eb-80e6-394f2e8e833c.png)

![2021-03-04 (6)__01](https://user-images.githubusercontent.com/71768466/110245107-ef7a1500-7f87-11eb-9f72-04836b15196c.png)

![2021-03-04 (7)__01](https://user-images.githubusercontent.com/71768466/110245110-f143d880-7f87-11eb-869e-65c524efedaa.png)

![2021-03-04 (8)__01](https://user-images.githubusercontent.com/71768466/110245115-f43ec900-7f87-11eb-8df2-edf87604e878.png)

![2021-03-04 (9)__01](https://user-images.githubusercontent.com/71768466/110245118-f6088c80-7f87-11eb-8cb9-0d297ac3ae57.png)

![2021-03-04 (13)__01](https://user-images.githubusercontent.com/71768466/110245122-f99c1380-7f87-11eb-9561-a4811de0fca1.png)

![2021-03-04 (14)__01](https://user-images.githubusercontent.com/71768466/110245124-fbfe6d80-7f87-11eb-9332-a7051b6ec5f5.png)

![2021-03-04 (15)__01](https://user-images.githubusercontent.com/71768466/110245127-fef95e00-7f87-11eb-81b0-8ec037e12c6b.png)

![2021-03-04 (16)__01](https://user-images.githubusercontent.com/71768466/110245132-01f44e80-7f88-11eb-87c7-f8a5603adbde.png)

![2021-03-04 (21)__01](https://user-images.githubusercontent.com/71768466/110245139-0587d580-7f88-11eb-8516-3ebb9f999ed0.png)

![2021-03-04 (22)__01](https://user-images.githubusercontent.com/71768466/110245140-07ea2f80-7f88-11eb-9695-fb483d5304f4.png)

![2021-03-04__01](https://user-images.githubusercontent.com/71768466/110245144-09b3f300-7f88-11eb-8d11-56a3e05ca7b5.png)

![2021-03-05 (2)__01](https://user-images.githubusercontent.com/71768466/110245155-10426a80-7f88-11eb-8618-c2b922539ce7.png)

![2021-03-05 (3)__01__01__01](https://user-images.githubusercontent.com/71768466/110245158-133d5b00-7f88-11eb-962f-3c05a69a7f41.png)

![2021-03-05 (4)__01](https://user-images.githubusercontent.com/71768466/110245165-159fb500-7f88-11eb-807d-324f30089e75.png)

![2021-03-05 (5)__01](https://user-images.githubusercontent.com/71768466/110245168-1afcff80-7f88-11eb-87a8-1e4371f38e50.png)

![2021-03-05 (6)__01](https://user-images.githubusercontent.com/71768466/110245174-1df7f000-7f88-11eb-8c0b-be95a1b654b0.png)

![2021-03-05 (7)__01](https://user-images.githubusercontent.com/71768466/110245175-205a4a00-7f88-11eb-8226-f6451faee642.png)

![2021-03-05 (10)__01](https://user-images.githubusercontent.com/71768466/110245180-26502b00-7f88-11eb-97d0-d50449b5a310.png)

![2021-03-05 (11)__01](https://user-images.githubusercontent.com/71768466/110245184-28b28500-7f88-11eb-9948-20e176caef3e.png)

![2021-03-05 (12)__01](https://user-images.githubusercontent.com/71768466/110245188-2b14df00-7f88-11eb-9739-e08a6a2d1cb8.png)

![2021-03-05__01](https://user-images.githubusercontent.com/71768466/110245190-2e0fcf80-7f88-11eb-8508-e001c230d122.png)

![2021-03-06 (2)__01](https://user-images.githubusercontent.com/71768466/110245194-349e4700-7f88-11eb-9ec4-5e8f00628828.png)

![2021-03-06 (4)__01](https://user-images.githubusercontent.com/71768466/110245198-3700a100-7f88-11eb-809a-8fe739b20dd1.png)

![2021-03-06 (5)__01](https://user-images.githubusercontent.com/71768466/110245201-3962fb00-7f88-11eb-8c64-f7a22acfcf5b.png)

![2021-03-06 (6)__01](https://user-images.githubusercontent.com/71768466/110245204-3bc55500-7f88-11eb-9878-f227d7ae7f8e.png)

![2021-03-06 (7)__01](https://user-images.githubusercontent.com/71768466/110245207-3e27af00-7f88-11eb-895b-06edcbc982dc.png)

![2021-03-06 (9)__01](https://user-images.githubusercontent.com/71768466/110245215-42ec6300-7f88-11eb-8c00-a318c03d4020.png)

![2021-03-06 (10)__01](https://user-images.githubusercontent.com/71768466/110245221-44b62680-7f88-11eb-9afd-d2246dfa2087.png)

![2021-03-06 (11)__01](https://user-images.githubusercontent.com/71768466/110245225-47188080-7f88-11eb-8444-ee8160ab85e3.png)

![2021-03-06 (12)__01](https://user-images.githubusercontent.com/71768466/110245229-4a137100-7f88-11eb-8c1e-e49ff656bc72.png)

![2021-03-06 (13)__01](https://user-images.githubusercontent.com/71768466/110245235-4d0e6180-7f88-11eb-8b45-7b719937731c.png)

![2021-03-06 (14)__01](https://user-images.githubusercontent.com/71768466/110245238-50095200-7f88-11eb-875b-e194d7339daa.png)

![2021-03-07 (2)__01](https://user-images.githubusercontent.com/71768466/110245244-5b5c7d80-7f88-11eb-998f-43908e5fe7a5.png)

![2021-03-07__01](https://user-images.githubusercontent.com/71768466/110245248-5e576e00-7f88-11eb-98de-1c83f38e32e9.png)



