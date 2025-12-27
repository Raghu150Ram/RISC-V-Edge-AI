## Day 1: Edge AI Motivation, RISC-V Hardware Overview, and Freedom Studio Setup

Day 1 focused on understanding the need for Edge AI on low-compute, resource-constrained chips, followed by learning the hardware specifications of the VSDSquadron Pro Board and setting up essential software tools such as Freedom Studio on both desktop and cloud-based environments.

<img width="960" height="500" alt="image" src="https://github.com/user-attachments/assets/78205202-e241-4d87-8763-c07a8f54c9c8" />

<br>
<br>

<details>
<summary><strong>Edge AI Orientation and Hardware Features</strong></summary>

<br>

- Challenges faced and the need for Edge AI:
<img width="960" height="500" alt="image" src="https://github.com/user-attachments/assets/67967f6b-fea7-4dc8-9a8f-77d940369f95" />

<br>
<br>

- VSDSquadron PRO Board Components:
<img width="960" height="550" alt="image" src="https://github.com/user-attachments/assets/c8d36606-7c19-40f7-9528-b7a320a59d01" />
<img width="960" height="550" alt="image" src="https://github.com/user-attachments/assets/44f29bfa-9fbd-42e5-95da-82d5fe3bb074" />

The board features a 32-bit RV32IMAC core and a 16KB L1 Instruction Cache and a 16KB Data SRAM scratchpad.
<br>

- Detail Specifications of the VSDSquadron PRO Board:
<img width="960" height="550" alt="image" src="https://github.com/user-attachments/assets/3058d48d-bdd5-4be9-af70-90591dc35a04" />

</details>

<details>
<summary><strong>Installation Requirements and Procedure</strong></summary>

- Create a Google Collab account for making the python scripts.

<details>
  <summary>Freedom Studio Installation: Desktop</summary>

  - If you are using the physical board to run your programs, follow 'Step 2: Installation and Settings' in the Datasheet (page 10) uploaded in the folder. This will guide you through the installation of the Freedom Studio Software and test your setup by running the “sifive-welcome” example program.
    - If you face SDK issues:

      a. Download the SDK: [Link](Freedom E SDK v21.11.00.00 from https://vsd-labs.sgp1.cdn.digitaloceanspaces.com/vsd-labs/freedom-e-sdk-v21.11.00.00.zip)

      b. Extract the contents.
      
      c. Update the SDK path to this folder while creating the project.
  - If you are using the Emulator (Online Simulation Software), the follow the following steps:

    1. Select Target as 'qemu-sifive-e31' instead of 'sifive-hifive1'

        <img width="890" height="650" alt="image" src="https://github.com/user-attachments/assets/ce75068b-23f7-4337-8db3-dfb6b73d4eab" />

    2. If there are any errors, check for:
       - Project (Tool Bar) -> Properties -> Freedom Studio -> QEMU Path - has the path available, else choose 'select from list' (or) choose the 'Browse' option and choose the following address: '...\VSDSquadronPRO\FreedomStudio-3-1-1-x86_64-w64-mingw32\FreedomStudio-3-1-1\SiFive\riscv-qemu-6.0.0-2021.11.5\bin\qemu-system-riscv32.exe'
        <br>
        
        <img width="890" height="583" alt="image" src="https://github.com/user-attachments/assets/9cfd731a-1533-4baf-84be-555505d64967" />
        <br>

       - In the 'Project Explorer' -> bsp -> settings.mk -> change 'RISCV_ARCH = rv32imac' to RISCV_ARCH = rv32imac_zicsr_zifencei
        <br>
        
        <img width="890" height="457" alt="image" src="https://github.com/user-attachments/assets/3c720150-130e-4e6f-a30a-83052e25ae80" />

    3. Now, Your code should be able to build without any errors.

</details>

<details>
  <summary>Freedom Studio Installation: Cloud</summary>

  - To use the Cloud resources, follow the steps given in the 'README.mk' file in the following repository: [Cloud_Repository](https://github.com/vsdip/vsd-riscv-edgeai)
    - The repository was devloped by VSD.
  - Now the software is setup successfully and ready to use.
    
</details>
</details>

<details>
<summary><strong>Datasets</strong></summary>

- For the Workshop, we will be primarily using 3 datasets: _'Student Scores.csv', '50 Startups.csv', 'Social Network Ads.csv'_.
- The above datasets are avaialable in this folder with the same names as mentioned above. 

</details>

---

### Key Takeaway
This day set the stage for the rest of the workshop by providing an orientation on the need for Edge AI, followed by the installation and testing of the required software and downloading all the necessary documentation.
