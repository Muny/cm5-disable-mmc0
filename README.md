# cm5-disable-mmc0

1. Compile the overlay:
    ```console
    $ dtc -@ -Hepapr -I dts -O dtb -o disable-mmc0.dtbo disable-mmc0.dts
    ```

2. Copy the overlay to `/boot/firmware/overlays/`:
    ```console
    $ sudo cp disable-mmc0.dtbo /boot/firmware/overlays/
    ```

3. Add the overlay to `/boot/firmware/config.txt`:
    ```
    dtoverlay=disable-mmc0
    ```

4. Reboot