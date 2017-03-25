Ansible Role: tlp
=================

[![Build Status](https://travis-ci.org/Anthony25/ansible-role-tlp.svg?branch=master)](https://travis-ci.org/Anthony25/ansible-role-tlp)

Ansible role to install and configure tlp.

Role Variables
--------------

```yaml
tlp_enable: true

tlp_default_mode: "AC"

tlp_disk_idle_secs:
  ac: 0
  bat: 2

tlp_max_lost_work_secs:
  ac: 15
  bat: 60

tlp_cpu_scaling_governor:
  ac: "powersave"
  bat: "powersave"

tlp_cpu_scaling_min_freq:
  ac:
  bat:
tlp_cpu_scaling_min_freq:
  ac:
  bat:

tlp_cpu_min_perf:
  ac:
  bat:
tlp_cpu_max_perf:
  ac:
  bat:

tlp_cpu_boost:
  ac:
  bat:

tlp_sched_powersave:
  ac: 0
  bat: 1

tlp_nmi_watchdog: 0
tlp_phc_controls:

tlp_energy_perf_policy:
  ac: "performance"
  bat: "powersave"

tlp_disk_devices: "sda sdb"

tlp_disk_apm_level:
  ac: "254 254"
  bat: "128 128"

tlp_disk_spindown_timeout:
  ac:
  bat:

tlp_disk_iosched:

tlp_sata_linkpwr:
  ac: "max_performance"
  bat: "min_power"
tlp_sata_linkpwr_blacklist:

tlp_ahci_runtime_pm:
  ac:
  bat:
tlp_ahci_runtime_pm_timeout: 15

tlp_pcie_aspm:
  ac: "performance"
  bat: "powersave"

tlp_radeon_power_profile:
  ac: "high"
  bat: "low"

tlp_radeon_dpm_state:
  ac: "performance"
  bat: "battery"

tlp_radeon_dpm_perf_level:
  ac: "auto"
  bat: "auto"

tlp_wifi_pwr:
  ac: "off"
  bat: "on"

tlp_wol_disable: "Y"

tlp_sound_power_save:
  ac: 0
  bat: 1
tlp_sound_power_save_controller: "Y"

tlp_bay_poweroff:
  bat: 0
tlp_bay_device: "sr0"

tlp_runtime_pm:
  ac: "on"
  bat: "auto"
tlp_runtime_pm_all: 1
tlp_runtime_pm_blacklist:
tlp_runtime_pm_driver_blacklist: "radeon nouveau"

tlp_usb_autosuspend: 1
tlp_usb_blacklist:
tlp_usb_whitelist:
tlp_usb_blacklist_wwan: 1
tlp_usb_autosuspend_disable:
  shutdown:

tlp_restore_device_state:
  startup: 0
tlp_devices_to_disable:
  startup:
  shutdown:
  bat:
  bat_not_in_use:
  lan_connect:
  wifi_connect:
  wwan_connect:
  dock:
  undock:

tlp_devices_to_enable:
  startup:
  shutdown:
  ac:
  lan_connect:
  wifi_connect:
  wwan_connect:
  dock:
  undock:

tlp_charge_thresh:
  BAT0:
    start:
    stop:
```

The variables naming logic is to define a dict when the option relies on a
state (for example `CPU_BOOST_ON_AC` and `CPU_BOOST_ON_BAT`).

All empty variables listed before are just here for the documentation. They
are not defined in `defaults/main.yml`.

It is possible that a new option brought by a new TLP release would be missing
here, so do not hesitate to open an issue to request it.

Dependencies
------------

None

License
-------

Tool under the BSD license. Do not hesitate to report bugs, ask me some
questions or do some pull request if you want to!
