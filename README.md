# Windows-11-on-termux
Full size 4 gb are you sure






pkg install x11-repo
pkg upgrade
pkg install qemu-system-aarch64 qemu-utils libslirp
qemu-img create -f qcow2 win11.img 100G
termux-setup-storage
adb push win11arm.iso /sdcard/Download
adb push QEMU_EFI.fd /sdcard/Download

qemu-system-aarch64 -m 2048 -cpu cortex-a72 -smp 4 -M virt -nographic -bios storage/downloads/QEMU_EFI.fd -drive if=none,file=win11.img,id=hd0 -device virtio-blk-device,drive=hd0 -netdev user,id=n0 -vnc 127.0.0.1:3 -cdrom storage/downloads/win11arm.iso.    





download for now :)

win11arm.iso https://drive-google-com.translate.goog/file/d/1Yx_AA-fRT1mXFh5t1w2VLkGTX_Z-l8jL/view?_x_tr_sl=en&_x_tr_tl=id&_x_tr_hl=id&_x_tr_pto=tc




qemu efi fb 


https://drive-google-com.translate.goog/file/d/13ZP1itNl6riAa7jY90TzX1KDZPoMzhWi/view?_x_tr_sl=en&_x_tr_tl=id&_x_tr_hl=id&_x_tr_pto=tc
