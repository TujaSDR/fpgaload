# fpgaload

Python script to load the FPGA binary on Tuja.
First enable SPI, use `raspi-config` or uncomment this line in `/boot/config.txt`:

```
#dtparam=spi=on
```

You probably need to update `spidev`.

```bash
pip3 install spidev
```

Place `fpgaload` in your path.

## Usage

```bash
# Read RBF from file:
fpgalaod tujadev.rbf

# Read RBF from stdin:
fpgalaod < tujadev.rbf

# Program over SSH
cat tujadev.rbf|ssh pi@sdr.local fpgaload
```
