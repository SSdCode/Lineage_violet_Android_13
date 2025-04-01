# Clone device tree

samir@samir-OMEN-by-HP-Gaming-Laptop-16-wf1xxx:~/AOSP/Redmi note 7 pro/Android 13 Lineage 20$ git clone https://github.com/LineageOS/android_device_xiaomi_violet.git -b lineage-20 device/xiaomi/violet
Cloning into 'device/xiaomi/violet'...
remote: Enumerating objects: 20139, done.
remote: Counting objects: 100% (2688/2688), done.
remote: Compressing objects: 100% (1000/1000), done.
remote: Total 20139 (delta 1310), reused 2655 (delta 1287), pack-reused 17451 (from 1)
Receiving objects: 100% (20139/20139), 20.26 MiB | 3.07 MiB/s, done.
Resolving deltas: 100% (12647/12647), done.

//dependency for device/xiaomi/violet
samir@samir-OMEN-by-HP-Gaming-Laptop-16-wf1xxx:~/AOSP/Redmi note 7 pro/Android 13 Lineage 20$ git clone https://github.com/LineageOS/android_device_xiaomi_sm6150-common.git -b lineage-20 device/xiaomi/sm6150-common
Cloning into 'device/xiaomi/sm6150-common'...
remote: Enumerating objects: 24795, done.
remote: Counting objects: 100% (2855/2855), done.
remote: Compressing objects: 100% (457/457), done.
remote: Total 24795 (delta 2609), reused 2398 (delta 2398), pack-reused 21940 (from 4)
Receiving objects: 100% (24795/24795), 6.90 MiB | 3.09 MiB/s, done.
Resolving deltas: 100% (16238/16238), done.

**********************************************************************************************************************************

# Clone kernel

samir@samir-OMEN-by-HP-Gaming-Laptop-16-wf1xxx:~/AOSP/Redmi note 7 pro/Android 13 Lineage 20$ git clone https://github.com/LineageOS/android_kernel_xiaomi_sm6150.git -b lineage-20 kernel/xiaomi/sm6150
Cloning into 'kernel/xiaomi/sm6150'...
remote: Enumerating objects: 6475442, done.
remote: Total 6475442 (delta 0), reused 0 (delta 0), pack-reused 6475442 (from 1)
Receiving objects: 100% (6475442/6475442), 1.24 GiB | 2.12 MiB/s, done.
Resolving deltas: 100% (5379234/5379234), done.
Updating files: 100% (72349/72349), done.
samir@samir-OMEN-by-HP-Gaming-Laptop-16-wf1xxx:~/AOSP/Redmi note 7 pro/Android 13 Lineage 20$ 

// Not needed below
// LineageOS kernel for android 13 is not available so cloning from pixel Experience and will modify for lineage 

samir@samir-OMEN-by-HP-Gaming-Laptop-16-wf1xxx:~/AOSP/Redmi note 7 pro/Android 13 Lineage 20$ git clone https://github.com/PixelExperience-Devices/kernel_xiaomi_violet.git -b thirteen kernel/xiaomi/violet
Cloning into 'kernel/xiaomi/violet'...
remote: Enumerating objects: 6424210, done.
remote: Counting objects: 100% (3621/3621), done.
remote: Compressing objects: 100% (802/802), done.
Receiving objects: 100% (6424210/6424210), 1.73 GiB | 2.39 MiB/s, done.
remote: Total 6424210 (delta 2921), reused 3456 (delta 2814), pack-reused 6420589 (from 1)
Resolving deltas: 100% (5169207/5169207), done.
Updating files: 100% (70231/70231), done.
samir@samir-OMEN-by-HP-Gaming-Laptop-16-wf1xxx:~/AOSP/Redmi note 7 pro/Android 13 Lineage 20$ 


**********************************************************************************************************************************

# Clone vendor blobs

samir@samir-OMEN-by-HP-Gaming-Laptop-16-wf1xxx:~/AOSP/Redmi note 7 pro/Android 13 Lineage 20$ git clone https://github.com/xiaomi-sm6150/proprietary_vendor_xiaomi_violet.git -b lineage-20 vendor/xiaomi/violet
Cloning into 'vendor/xiaomi/violet'...
remote: Enumerating objects: 376, done.
remote: Counting objects: 100% (11/11), done.
remote: Compressing objects: 100% (9/9), done.
remote: Total 376 (delta 3), reused 2 (delta 2), pack-reused 365 (from 2)
Receiving objects: 100% (376/376), 156.14 MiB | 1.64 MiB/s, done.
Resolving deltas: 100% (172/172), done.
Updating files: 100% (330/330), done.
samir@samir-OMEN-by-HP-Gaming-Laptop-16-wf1xxx:~/AOSP/Redmi note 7 pro/Android 13 Lineage 20$ 


samir@samir-OMEN-by-HP-Gaming-Laptop-16-wf1xxx:~/AOSP/Redmi note 7 pro/Android 13 Lineage 20$ git clone https://github.com/xiaomi-sm6150/proprietary_vendor_xiaomi_sm6150-common.git -b lineage-20 vendor/xiaom
i/sm6150-common
Cloning into 'vendor/xiaomi/sm6150-common'...
remote: Enumerating objects: 1223, done.
remote: Counting objects: 100% (26/26), done.
remote: Compressing objects: 100% (21/21), done.
remote: Total 1223 (delta 6), reused 8 (delta 5), pack-reused 1197 (from 3)
Receiving objects: 100% (1223/1223), 166.31 MiB | 855.00 KiB/s, done.
Resolving deltas: 100% (431/431), done.
samir@samir-OMEN-by-HP-Gaming-Laptop-16-wf1xxx:~/AOSP/Redmi note 7 pro/Android 13 Lineage 20$ 

**********************************************************************************************************************************

# Clone hardware Xiaomi

samir@samir-OMEN-by-HP-Gaming-Laptop-16-wf1xxx:~/AOSP/Redmi note 7 pro/Android 13 Lineage 20$ git clone https://github.com/LineageOS/android_hardware_xiaomi.git -b lineage-20 hardware/xiaomi
Cloning into 'hardware/xiaomi'...
remote: Enumerating objects: 1645, done.
remote: Counting objects: 100% (27/27), done.
remote: Compressing objects: 100% (9/9), done.
remote: Total 1645 (delta 21), reused 18 (delta 18), pack-reused 1618 (from 2)
Receiving objects: 100% (1645/1645), 407.45 KiB | 2.75 MiB/s, done.
Resolving deltas: 100% (877/877), done.
samir@samir-OMEN-by-HP-Gaming-Laptop-16-wf1xxx:~/AOSP/Redmi note 7 pro/Android 13 Lineage 20$ 





To fix compilation errors edited below files





