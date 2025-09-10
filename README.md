# Test-Repo

cp ../../kernel_patches/next/susfs_fix_patches/v1.5.9/fix_apk_sign.c.patch ./
              patch -p1 --forward < fix_apk_sign.c.patch
              
              cp ../../kernel_patches/next/susfs_fix_patches/v1.5.9/fix_core_hook.c.patch ./
              patch -p1 --forward --fuzz=3 < fix_core_hook.c.patch
              
              cp ../../kernel_patches/next/susfs_fix_patches/v1.5.9/fix_selinux.c.patch ./
              patch -p1 --forward < fix_selinux.c.patch
              
              cp ../../kernel_patches/next/susfs_fix_patches/v1.5.9/fix_ksud.c.patch ./
              patch -p1 --forward < fix_ksud.c.patch

              cp ../../kernel_patches/next/susfs_fix_patches/v1.5.9/fix_rules.c.patch ./
              patch -p1 --forward < fix_rules.c.patch

              cp ../../kernel_patches/next/susfs_fix_patches/v1.5.9/fix_sucompat.c.patch ./
              patch -p1 --forward < fix_sucompat.c.patch

              cp ../../kernel_patches/next/susfs_fix_patches/v1.5.9/fix_kernel_compat.c.patch ./
              patch -p1 --forward < fix_kernel_compat.c.patch

              cp ./kernel_patches/KernelSU/10_enable_susfs_for_ksu.patch $KERNEL_REPO/KernelSU/
cp ./kernel_patches/50_add_susfs_in_gki-android14-6.1.patch $KERNEL_REPO/common/
cp ./kernel_patches/fs/* $KERNEL_REPO/common/fs/
cp ./kernel_patches/include/linux/* $KERNEL_REPO/common/include/linux/

cd $KERNEL_REPO/common
patch -p1 < 50_add_susfs_in_gki-android14-6.1.patch
cd $KERNEL_REPO/KernelSU
patch -p1 < 10_enable_susfs_for_ksu.patch

cp ./kernel_patches/50_add_susfs_in_gki-android14-6.1.patch $KERNEL_REPO/common/
cp ./kernel_patches/fs/* $KERNEL_REPO/common/fs/
cp ./kernel_patches/include/linux/* $KERNEL_REPO/common/include/linux/

cd $KERNEL_REPO/common
patch -p1 < 50_add_susfs_in_gki-android14-6.1.patch
