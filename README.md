# 4 Week Mini  research internship of VLSI using VSDSquadron Mini RISC-V Development kit
This repositiry is intended to document the learning outcomes and experience of a 4-week workshop on VLSI and RISC-V using VSDSquadron Mini RISC-V Development kit.

<details>
<summary>Introduction</summary>
<br>
Install required softwares for the program.Alloted space of 100 GB and 8 TB for Virtual machine and connected the ubuntu disc file with it. 
</details>

<details>
<summary> Software and OS needed</summary>
<br>
Ubuntu, Oracle Virtual Machine and packages needed are Yosys,gtkwave,iverilog,OpenSTA,Magic
</details>

<details>
  <summary> Yosys </summary>
  
  Installed all required Softwares for the project.
  <br>
  ![yosys](https://github.com/KumarKarthikeya/VLSI-VSD/assets/72381320/cdf2f054-2697-4348-8205-106470f96ec2)

</details>

<details>
  <summary>  gtkwave </summary>
  <code>sudo apt-get install gtkwave</code>
  
  gtkwave has also been installed using when insatlling the git file of VSD Open source EDA tools
  <br>
  ![gtkwave](https://github.com/KumarKarthikeya/VLSI-VSD/assets/72381320/b8e36f86-86c9-46b0-a7dd-42a560e43e0f)

</details>

<details>
  <summary> iverilog </summary>
<code>sudo apt-get install iverilog</code>
  
  Iverilog is been installed
  <br>
  ![iverilog](https://github.com/KumarKarthikeya/VLSI-VSD/assets/72381320/f683573b-262c-47a3-8c26-39d73d59114a)

</details>

<details>
  <summary> BLOCK DIAGRAM for Car parking system </summary>

 car parking system
  <br>
 ![block diagram](https://github.com/KumarKarthikeya/VLSI-VSD/assets/72381320/d6b9dbce-a84f-4767-beda-345a00c2d676)


</details>

<details>
  <summary> TASK 3: Installion of RTL and Test bench files and chexk the basic functional simulation. </summary>

  SKY 130
  <br>
  ![Screenshot from 2024-02-25 10-29-05](https://github.com/KumarKarthikeya/VLSI-VSD/assets/72381320/5cabf6a2-8980-4827-a887-2a74ef5a5fe2)

  RTL and TB files
  <br>
  ![Screenshot from 2024-02-25 10-29-18](https://github.com/KumarKarthikeya/VLSI-VSD/assets/72381320/67aef5b1-2dcc-4434-8f46-4ee820823777)

  Basis of functional simulation
  <br>
  ![Screenshot from 2024-02-25 13-36-48](https://github.com/KumarKarthikeya/VLSI-VSD/assets/72381320/7d5ead33-1c86-4262-b9d3-6f503af320e0)

</details>

<details>
  <summary> TASK 4:Read the example verilog file,synthesis and write the netlist.  </summary>

  Invoking yosys inside verilog_code file:
  
  <code>yosys</code>
  <br>
  ![yosys](https://github.com/KumarKarthikeya/VLSI-VSD/assets/72381320/7b476ff5-d367-4f64-82ba-88b6776e3079)

  Reading the Library:

  <code>read_liberty -lib /home/kumar123/sky130RTLDesignAndSynthesisWorkshop/lib/sky130_fd_sc_hd__tt_025C_1v80.lib</code>
  <br>
  ![read lib](https://github.com/KumarKarthikeya/VLSI-VSD/assets/72381320/06e8f261-67e4-4b90-a452-2cb12e2f8b44)

  Reading the Design:

  <code>read_verilog good_mux.v</code>
  <br>
  ![read verilog](https://github.com/KumarKarthikeya/VLSI-VSD/assets/72381320/30c76fdf-fdf5-4096-a4bd-e119ddaf82bd)

  Specifying the module that we are synthesizing:

  <code>synth -top good_mux</code>
  <br>
  ![synth](https://github.com/KumarKarthikeya/VLSI-VSD/assets/72381320/401752ce-8d5b-451f-b50b-346be328f5b4)

  To generate the netlist use abc liberty:

  <code>abc -liberty /home/kumar123/sky130RTLDesignAndSynthesisWorkshop/lib/sky130_fd_sc_hd__tt_025C_1v80.lib</code>
  <br>
  ![abc liberty](https://github.com/KumarKarthikeya/VLSI-VSD/assets/72381320/fc9fc79c-ac05-445e-ab89-547127a90ca5)

  To see the graphical version of the logic:

  <code>show</code>
  <br>
  ![show](https://github.com/KumarKarthikeya/VLSI-VSD/assets/72381320/17c7dc2d-cbc5-4b25-9182-7087d1d2f0f4)

  To write the netlist:

  <code>write_verilog good_mux_netlist.v</code>
  <br>
  ![write verilog](https://github.com/KumarKarthikeya/VLSI-VSD/assets/72381320/e2818095-8900-40ce-9e8c-758b6823e665)

  Using the switch '-noattr' to get the simplified version of netlist file:

  <code>write_verilog -noattr good_mux_netlist.v</code>
  <br>
  ![write verilog noattr](https://github.com/KumarKarthikeya/VLSI-VSD/assets/72381320/98236726-aeff-4243-a6bb-52a899ffdf0b)

  To open the netlist:

  <code>!gvim good_mux_netlist.v</code>
  <br>
  ![gvim](https://github.com/KumarKarthikeya/VLSI-VSD/assets/72381320/99c3eafe-2147-4070-8959-147d75b22bf4)

  ![gvim code](https://github.com/KumarKarthikeya/VLSI-VSD/assets/72381320/36b34545-5ce3-4788-831a-f8450153fd68)


</details>

<details>
  <summary> TASK 5: Read the project files and write the netlist and verify the wave forms. </summary>

  Extract the git code file to car parking system project
  <code> git clone https://github.com/ishan-desai64/iiitb_cps.git</code>
  <br>
  ![synth real](https://github.com/KumarKarthikeya/VLSI-VSD/assets/72381320/58e287d6-4019-4232-89d9-fcbc9a869ac3)
![abc lib real](https://github.com/KumarKarthikeya/VLSI-VSD/assets/72381320/5d9f74ce-e045-47b8-9d48-5f4b7346101d)
![representation oif cells](https://github.com/KumarKarthikeya/VLSI-VSD/assets/72381320/615372dc-ed19-4fb6-8478-1d1fae314959)
![gtk wave](https://github.com/KumarKarthikeya/VLSI-VSD/assets/72381320/69b08d2d-42a4-456b-957d-25de19db353d)
![git cline](https://github.com/KumarKarthikeya/VLSI-VSD/assets/72381320/35035520-064c-4966-bd4f-eab5c747d5fd)
![yosys real](https://github.com/KumarKarthikeya/VLSI-VSD/assets/72381320/4eb0464f-2fd0-41e4-bff8-10acecfa6637)
![read lib real](https://github.com/KumarKarthikeya/VLSI-VSD/assets/72381320/5c39e1bb-cf0a-4272-bad5-6b9a23b67624)
![read verilog real](https://github.com/KumarKarthikeya/VLSI-VSD/assets/72381320/ff09160b-11b2-496d-acd5-4dab3cc79ea9)

</details>
