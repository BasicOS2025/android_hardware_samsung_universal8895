# Experimental Android 17 / LineageOS 24 migration

Targets: Galaxy S8 SM-G950F (dreamlte), S8+ SM-G955F (dream2lte), Note8 SM-N950F (greatlte).

Upstream: https://codeberg.org/universal8895/android_hardware_samsung
Baseline branch: `lineage-23.0`. Baseline commit: `2abfdb1a286b11bd29140ae8ae61ac6ad0e81fb1`.

Status: initial migration, not yet verified by an Android 17 ROM build or phone boot.
Original licensing, authorship and source history are retained.
Build coordination: https://github.com/BasicOS2025/universal8895-lineage24-build

## Removed Android 17 HIDL interfaces

Legacy HIDL vibrator 1.0 and consumer IR 1.0 service build descriptions are
retained as Android.bp.legacy, outside Soong discovery. Android 17 no longer
supplies their interface modules. The universal8895 product selects the AIDL
android.hardware.vibrator-service.samsung instead and does not select consumer
IR. Source and license notices are retained for reference.
