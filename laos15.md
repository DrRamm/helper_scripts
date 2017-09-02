## # Importer command
#### #### source <(curl -Ls https://github.com/AdrianDC/lineage_development_sony8960_master/raw/local_manifests/repopick-lineage-15.0.md)

## # Gerrit without devices and kernels over lineage-15.0*
#### # https://review.lineageos.org/#/q/status:open+branch:%255Elineage-15.0.*+-project:%255ELineageOS/android_device_.*+-project:%255ELineageOS/android_kernel_.*


#### # source <(curl -Ls https://raw.githubusercontent.com/DrRamm/helper_scripts/drramm/laos15.md)

repopick 187865 187860;
#### # charger
repopick 187951;

#### # bt-caf
cd hardware/qcom/bt-caf && git fetch https://review.lineageos.org/LineageOS/android_hardware_qcom_bt refs/changes/64/187864/1 && git checkout FETCH_HEAD && cd ../../../;

#### # system_bt 
#### # p_inq->next_state += 1;
repopick 185858;

#### # tiny compress 
cd external/tinycompress && git fetch https://review.lineageos.org/LineageOS/android_external_tinycompress refs/changes/39/185939/1 && git checkout FETCH_HEAD && cd ../../;


#### # device/lineage/sepolicy
#########################repopick 188006;
