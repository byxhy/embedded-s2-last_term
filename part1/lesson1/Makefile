all: led.o 
    arm-linux-ld -Tled.lds -o led.elf $<
    arm-linux-objcopy -O binary led.elf led.bin
    
led.o : led.S
    arm-linux-gcc -g -o $@ -c $<
    
.PHONY: clean
clean: 
    rm -rf *.o led.elf led.bin


