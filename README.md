# Installing Quartus on Ubuntu (Tested on 20.04 LTS)

<!--- This is a comment. --->

## Download Quartus Web 13.1

Download [from this link](https://download.altera.com/akdlm/software/acdsinst/13.1/162/ib_tar/Quartus-web-13.1.0.162-linux.tar).

## Installing the 32-bit libraries

### Libraries to run the setup:

``` bash
sudo dpkg --add-architecture i386
```

``` bash
sudo apt update
```

``` bash
sudo apt-get install libstdc++5:i386 libmotif4:i386 libxp6:i386 libcurl4:i386
```

### Libraries to run the Quartus Web 13.1:

``` bash
sudo add-apt-repository ppa:linuxuprising/libpng12
```

``` bash
sudo apt update
```

``` bash
sudo apt install libpng12-0
```

## Installing Quartus Web 13.1

In download location **extract** the **.tar** files and open the setup with the following command:

``` bash
./setup.sh
```

The installation process should proceed normally.

## Running Quartus Web 13.1

Run Quartus with the following command:

``` bash
<install_path>/quartus/bin/quartus --64bit
```

To simplify, you can add the following alias to **.bashrc**:

``` bash
alias quartus='<install_path>/quartus/bin/quartus --64bit'
```

Now typing **quartus** in terminal will open the program.

## Additional Settings

By using Quartus it was possible to create a project and compile codes in VHDL. However, during simulations with the University Program VWF, an error occurred:

``` diff
- "ModelSim executable not found."
```

To solve this issue go to:

<pre>
Tools &#8594; Options &#8594; EDA Tool Options
</pre>

Only one field will have a link. And it's the wrong field! **Cut and paste the link into the ModelSim field**.
