# Msr605x
## Run
    ~ npm i
    ~ node index.js
### Linux not root
Create rules in /etc/udev/rules.d/50-msr605x.rules
    
    SUBSYSTEMS=="usb", ATTRS{idVendor}=="0801", ATTRS{idProduct}=="0003", MODE="0660", TAG+="uaccess"
## Comands
    * read -- prepare the card reader to read a card, outputs in Raw and ISO
    * read_cycle -- read repeatedly until execution halts
    * write_raw -- prepare to write a raw hex stream to the card. usage: write_raw track1/none track2/none track3/none
    * clone -- prepare to read a card, and upon read success, prepare to write another card with raw equivalent data
    * write_iso -- prepare to write ISO data to a card, usage: write_iso track1/none~track2/none~track3/none
    * 5dump -- Пятёрочка
    * write_script -- enables write_iso macro to be loaded
    * exit -- "exit"
## Оригинал: https://github.com/Protryon/misiri_driver



