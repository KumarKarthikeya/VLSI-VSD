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


Check the Gtkwave for the design

<code> iverilog iiitb_cps.v</code>
<code>./a.out</code>
<code>gtkwave iiitb_cps.vcd</code>
<br>
![gtkwave](https://github.com/KumarKarthikeya/VLSI-VSD/assets/72381320/91c7e561-947e-48f9-9c77-6e9d60f8e50a)

   To Generate the netlist extract the git code file of car parking system project
   
  <code> git clone https://github.com/ishan-desai64/iiitb_cps.git</code>
  <br>
  ![git cline](https://github.com/KumarKarthikeya/VLSI-VSD/assets/72381320/ce399d34-1943-420e-8b48-fcc6641e7dd0)

  Invoking yosys inside iiitb_cps file
  
<code>yosys</code>
<br>
![yosys real](https://github.com/KumarKarthikeya/VLSI-VSD/assets/72381320/9bde156a-1558-462d-879d-6e667e4c7501)

Reading the Library:

<code>read_liberty -lib /home/kumar123/iiitb_cps/lib/sky130_fd_sc_hd_tt_025C_ 1v80.lib</code>
<br>
![read lib real](https://github.com/KumarKarthikeya/VLSI-VSD/assets/72381320/40674605-992c-4594-b2be-9dd34df64d05)

Read verilog file:

<code>read_verilog iiitb_cps.v</code>
<br>
![read verilog real](https://github.com/KumarKarthikeya/VLSI-VSD/assets/72381320/7e51a141-cdd4-416f-812a-be4e05654e6c)

Synthesizing the project module:

<code>synth -top iiitb_cps</code>
<br>
![synth real](https://github.com/KumarKarthikeya/VLSI-VSD/assets/72381320/e3309e3a-f420-4b71-b0a3-507c51eaa55b)

Generate the netlist:

<code>abc -liberty /home/kumar123/iiitb_cps/lib/sky130_fd_sc_hd_tt_025C_1v80.lib</code>
<br>
![abc lib real](https://github.com/KumarKarthikeya/VLSI-VSD/assets/72381320/928219a8-95e1-4902-a113-99d4f422f6ad)

To write the netlist:

<code>write_verilog netlist.v</code>

Using the switch '-noattr' to get the simplified version of netlist file:

<code>write_verilog -noattr netlist.v</code>

To see graphical representation of the logic:
<code>show</code>
![show dot](https://github.com/KumarKarthikeya/VLSI-VSD/assets/72381320/ff7e6747-76f4-4ba3-8e59-d6a60df887c0)

To open the netlist:
<code>!gvim netlist.v</code>

Here is the clear view of circuit:

[output.pdf](https://github.com/KumarKarthikeya/VLSI-VSD/files/14545854/output.pdf)

Check the whether the netlist will match the design:
<code>iverilog ../iiitb_cps/verilog_model/primitives.v ../iiitb_cps/verilog_model/sky130_fd_sc_hd.v netlist.v iiitb_cps.v</code>

<code> ./a.out</code>

<code> gtkwave iiitb_cps.vcd</code>

Gtkwave of the netlist:
![gtk2](https://github.com/KumarKarthikeya/VLSI-VSD/assets/72381320/e3e5a93c-c1d4-4b1f-847e-4a6a68a79baa)



</details>
