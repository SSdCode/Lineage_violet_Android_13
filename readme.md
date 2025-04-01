# LineageOS 20 for Xiaomi Violet (Redmi Note 7 Pro)

This repository provides the necessary information and steps to set up LineageOS 20 (Android 13) for the Xiaomi Redmi Note 7 Pro (codename: `violet`). The device tree, kernel, vendor blobs, and hardware configurations are all separated into individual repositories for better management and scalability. This repository contains just the `README.md` to guide you through the setup process.

## Prerequisites

Before you begin, make sure you have the following:

- A Linux-based OS (Ubuntu or similar recommended).
- At least **100 GB** of free disk space.
- A proper environment set up for building AOSP, including:
  - Git
  - Repo
  - Java (OpenJDK 11)
  - Python 2.7 or 3.x
  - Other Android build dependencies (Check [AOSP build instructions](https://source.android.com/setup/build/requirements)).

## Repositories

This project is split across multiple Git repositories. The following repositories are used in this setup:

1. **Device Tree**: `android_device_xiaomi_violet`  
   - Contains device-specific configurations and setup for the Xiaomi Redmi Note 7 Pro.

2. **Common Device Tree**: `android_device_xiaomi_sm6150-common`  
   - Holds configurations that are shared among all Snapdragon 6150 devices.

3. **Kernel**: `android_kernel_xiaomi_sm6150`  
   - The kernel source for the Snapdragon 6150.

4. **Vendor Blobs**: `proprietary_vendor_xiaomi_violet`  
   - Contains proprietary blobs specific to the Xiaomi Redmi Note 7 Pro.

5. **Vendor Common Blobs**: `proprietary_vendor_xiaomi_sm6150-common`  
   - Contains common proprietary blobs for Snapdragon 6150 devices.

6. **Hardware**: `android_hardware_xiaomi`  
   - Includes hardware-specific configurations for Xiaomi devices.

## Setting Up the Project

Follow the steps below to clone the repositories and set up your local AOSP tree:

### 1. Initialize the Repo

Start by initializing the repo for your AOSP build:

```bash
repo init -u https://android.googlesource.com/platform/manifest -b android-13.0.0_r40
```

### 2. Clone Device, Kernel, Vendor, and Hardware Repositories

Now clone the necessary repositories:

#### Clone Device Tree

```bash
git clone https://github.com/LineageOS/android_device_xiaomi_violet.git -b lineage-20 device/xiaomi/violet
```

#### Clone Common Device Tree

```bash
git clone https://github.com/LineageOS/android_device_xiaomi_sm6150-common.git -b lineage-20 device/xiaomi/sm6150-common
```

#### Clone Kernel

```bash
git clone https://github.com/LineageOS/android_kernel_xiaomi_sm6150.git -b lineage-20 kernel/xiaomi/sm6150
```

#### Clone Vendor Blobs

```bash
git clone https://github.com/xiaomi-sm6150/proprietary_vendor_xiaomi_violet.git -b lineage-20 vendor/xiaomi/violet
```

#### Clone Common Vendor Blobs

```bash
git clone https://github.com/xiaomi-sm6150/proprietary_vendor_xiaomi_sm6150-common.git -b lineage-20 vendor/xiaomi/sm6150-common
```

#### Clone Hardware Xiaomi

```bash
git clone https://github.com/LineageOS/android_hardware_xiaomi.git -b lineage-20 hardware/xiaomi
```

### 3. Set Up Submodules (If Necessary)

If your project is using submodules, make sure to initialize them with:

```bash
git submodule init
git submodule update
```

### 4. Build the AOSP

Once all repositories are cloned, it's time to set up the build environment and start building:

#### Source the Build Environment

```bash
source build/envsetup.sh
```

#### Choose the Device

```bash
lunch lineage_violet-userdebug
```

#### Start the Build

```bash
make -j$(nproc --all)
```

This will begin building your AOSP-based LineageOS 20 for the Xiaomi Redmi Note 7 Pro.

## Troubleshooting

If you encounter any issues, here are some tips:

- Make sure all dependencies are installed and up-to-date.
- Double-check your repository URLs and branches.
- Ensure you have enough disk space, as the build can consume a large amount of space.

For further help, you can consult the [LineageOS Wiki](https://wiki.lineageos.org/) or the relevant device-specific forums.

## License

This project uses the AOSP code, which is licensed under the Apache License, Version 2.0. Please refer to the individual repositories for their respective licenses.

---

Feel free to modify and extend this `README.md` as needed for your project or if you need to include additional setup details!
