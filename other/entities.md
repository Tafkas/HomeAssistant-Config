# Home Assistant Entities

Query:

```py
{ % set
ents = states | sort(attribute='entity_id') %}
Total: {{ents | count}} entities

{ % for domain, group in ents | groupby('domain') %}
# {{ domain }} ({{ group | count }})
    { % for s in group %}
        - {{s.entity_id}} | {{s.name}} | {{s.state}}
        { % if s.attributes.unit_of_measurement %} 
            {{s.attributes.unit_of_measurement}}
        { % endif %}
        { % if area_name(s.entity_id) %} | area: {{area_name(s.entity_id)}}
        { % endif %}
    { % endfor %}
{ % endfor %}
```

## automation (45)

- automation.bedroom_co2_is_high | Bedroom CO2 Monitor | unavailable
- automation.co2_monitor_all_rooms | CO2 Monitor – All Rooms | on
- automation.daily_energy_report | Daily Energy Report | unavailable
- automation.daily_energy_report_2 | Daily Energy Report | unavailable
- automation.daily_energy_report_4 | Daily Energy Report | on
- automation.daily_weather_report | Daily Weather Report | unavailable
- automation.daily_weather_report_2 | Daily Weather Report | unavailable
- automation.daily_weather_report_3 | Daily Weather Report | unavailable
- automation.daily_weather_report_4 | Daily Weather Report | unavailable
- automation.daily_weather_report_5 | Daily Weather Report | unavailable
- automation.daily_weather_report_6 | Daily Weather Report | on
- automation.dishwasher_boolean_watchdog | Dishwasher boolean watchdog | unavailable
- automation.dishwasher_finished | Dishwasher finished (power-based) | on
- automation.dishwasher_ready | Dishwasher ready | unavailable
- automation.dishwasher_ready_2 | Dishwasher ready | unavailable
- automation.dishwasher_running_failsafe_reset | Dishwasher running failsafe reset | on
- automation.dishwasher_started | Dishwasher started (power-based) | on
- automation.dishwasher_startup_recovery | Dishwasher startup recovery | on
- automation.ebike_daily_reset | Ebike – Daily reset | on
- automation.ebike_start_on_off_peak_backup | Ebike – Start on off-peak backup | on
- automation.ebike_start_on_solar_excess | Ebike – Start on solar excess | on
- automation.ebike_stop_on_low_solar | Ebike – Stop on low solar | on
- automation.ebike_stop_when_daily_target_reached | Ebike – Stop when daily target reached | unavailable
- automation.ebike_stop_when_peak_demand_starts | Ebike – Stop when peak demand starts | on
- automation.ebike_stop_when_power_90_w | Ebike – Stop when power < 90 W | on
- automation.ebike_sync_state_with_manual_switch | Ebike – Sync state with manual switch | on
- automation.ebike_track_last_on_off_times | Ebike – Track last ON/OFF times | on
- automation.hans_night_light_off | Hans Night Light Off | unavailable
- automation.hans_night_light_off_2 | Hans Night Light Off | on
- automation.iphone_12_pro_left_home_notification | iPhone 12 Pro Left Home Notification | unavailable
- automation.iphone_12_pro_location_change | iPhone 12 Pro Location Change | on
- automation.kids_room_co2_is_high | Kids Room CO2 Monitor | unavailable
- automation.laundry_finished | Laundry finished | unavailable
- automation.laundry_finished_2 | Laundry finished | unavailable
- automation.laundry_finished_3 | Laundry finished | on
- automation.laundry_started | Laundry started | on
- automation.low_battery_and_maintenance_alert | Low Battery and Maintenance Alert | unavailable
- automation.low_battery_and_maintenance_alert_2 | Low Battery and Maintenance Alert | on
- automation.monthly_energy_report | Monthly Energy Report | unavailable
- automation.monthly_energy_report_2 | Monthly Energy Report | on
- automation.new_automation | Living Room CO2 Monitor | unavailable
- automation.notify_on_first_solar_export_of_the_day | Notify on First Solar Export of the Day | on
- automation.office_co2_is_high | Office CO2 Monitor | unavailable
- automation.reset_solar_export_daily_flag | Reset Solar Export Daily Flag | on
- automation.rfid_run_shelly_plug_for_1_hour_and_notify | RFID – Run Shelly Plug for 1 hour and notify | on

## binary_sensor (47)

- binary_sensor.auto_backup_backup_status | Auto Backup Backup status | off | area: Office
- binary_sensor.diskstation_cache_device_1_below_min_remaining_life | DiskStation (Cache device 1) Below min remaining
  life | off | area: Office
- binary_sensor.diskstation_cache_device_1_exceeded_max_bad_sectors | DiskStation (Cache device 1) Exceeded max bad
  sectors | off | area: Office
- binary_sensor.diskstation_cache_device_2_below_min_remaining_life | DiskStation (Cache device 2) Below min remaining
  life | off | area: Office
- binary_sensor.diskstation_cache_device_2_exceeded_max_bad_sectors | DiskStation (Cache device 2) Exceeded max bad
  sectors | off | area: Office
- binary_sensor.diskstation_drive_1_below_min_remaining_life | DiskStation (Drive 1) Below min remaining life | off |
  area: Office
- binary_sensor.diskstation_drive_1_exceeded_max_bad_sectors | DiskStation (Drive 1) Exceeded max bad sectors | off |
  area: Office
- binary_sensor.diskstation_drive_2_below_min_remaining_life | DiskStation (Drive 2) Below min remaining life | off |
  area: Office
- binary_sensor.diskstation_drive_2_exceeded_max_bad_sectors | DiskStation (Drive 2) Exceeded max bad sectors | off |
  area: Office
- binary_sensor.diskstation_drive_3_below_min_remaining_life | DiskStation (Drive 3) Below min remaining life | off |
  area: Office
- binary_sensor.diskstation_drive_3_exceeded_max_bad_sectors | DiskStation (Drive 3) Exceeded max bad sectors | off |
  area: Office
- binary_sensor.diskstation_drive_4_below_min_remaining_life | DiskStation (Drive 4) Below min remaining life | off |
  area: Office
- binary_sensor.diskstation_drive_4_exceeded_max_bad_sectors | DiskStation (Drive 4) Exceeded max bad sectors | off |
  area: Office
- binary_sensor.diskstation_security_status | DiskStation Security status | off | area: Office
- binary_sensor.fritz_box_7590_ax_connection | FRITZ!Box 7590 AX Connection | on | area: Office
- binary_sensor.fritz_box_7590_ax_link | FRITZ!Box 7590 AX Link | on | area: Office
- binary_sensor.fritz_box_7590_ax_wan_status | FRITZ!Box 7590 AX WAN status | on | area: Office
- binary_sensor.fritz_box_7590_ax_wan_status_2 | FRITZ!Box 7590 AX WAN status | on | area: Office
- binary_sensor.iphone_12_pro_focus | iPhone 12 Pro Focus | off
- binary_sensor.living_room_station_bedroom_connectivity | Netatmo Bedroom Connectivity | on | area: Bedroom
- binary_sensor.living_room_station_connectivity | Netatmo Living Room Connectivity | on | area: Living Room
- binary_sensor.living_room_station_hans_connectivity | Netatmo Hans Connectivity | on | area: Kids Rooms
- binary_sensor.living_room_station_office_connectivity | Netatmo Office Connectivity | on | area: Office
- binary_sensor.living_room_station_outdoor_module_connectivity | Netatmo Balcony Connectivity | on | area: Balcony
- binary_sensor.living_room_station_rain_gauge_connectivity | Netatmo Rain Gauge Connectivity | on | area: Balcony
- binary_sensor.living_room_station_smart_anemometer_connectivity | Netatmo Anemometer Connectivity | on | area: Balcony
- binary_sensor.roborock_qrevo_pro_charging | Roborock Qrevo Pro Charging | on | area: Office
- binary_sensor.roborock_qrevo_pro_cleaning | Roborock Qrevo Pro Cleaning | off | area: Office
- binary_sensor.roborock_qrevo_pro_dock_mop_drying | Roborock Qrevo Pro Dock Mop drying | off | area: Office
- binary_sensor.roborock_qrevo_pro_mop_attached | Roborock Qrevo Pro Mop attached | on | area: Office
- binary_sensor.roborock_qrevo_pro_water_box_attached | Roborock Qrevo Pro Water box attached | on | area: Office
- binary_sensor.roborock_qrevo_pro_water_shortage | Roborock Qrevo Pro Water shortage | off | area: Office
- binary_sensor.rpi_power_status | RPi Power status | off
- binary_sensor.shellyplugsg3_28372f2f1e04_overcurrent | Shelly Plug S (E-Bike) Overcurrent | off | area: Office
- binary_sensor.shellyplugsg3_28372f2f1e04_overheating | Shelly Plug S (E-Bike) Overheating | off | area: Office
- binary_sensor.shellyplugsg3_28372f2f1e04_overpowering | Shelly Plug S (E-Bike) Overpowering | off | area: Office
- binary_sensor.shellyplugsg3_28372f2f1e04_overvoltage | Shelly Plug S (E-Bike) Overvoltage | off | area: Office
- binary_sensor.shellyplusplugs_d4d4da363900_overcurrent | Shelly Plug S (Office) Overcurrent | off | area: Office
- binary_sensor.shellyplusplugs_d4d4da363900_overheating | Shelly Plug S (Office) Overheating | off | area: Office
- binary_sensor.shellyplusplugs_d4d4da363900_overpowering | Shelly Plug S (Office) Overpowering | off | area: Office
- binary_sensor.shellyplusplugs_d4d4da363900_overvoltage | Shelly Plug S (Office) Overvoltage | off | area: Office
- binary_sensor.stades_ipad_focus | Stade’s iPad Focus | off
- binary_sensor.yeelight_ceilc_0x178697e2_nightlight | Yeelight Living Room Nightlight | unavailable | area: Living Room
- binary_sensor.yeelight_ceilc_0x1786992c_nightlight | Yeelight Dining Room Nightlight | unavailable | area: Living Room
- binary_sensor.yeelight_ceiling11_0x101c56f2_nightlight | Yeelight Ceiling Light (Bed Room) Nightlight | unavailable |
  area: Bedroom
- binary_sensor.yeelight_ceiling11_0x66a47e6_nightlight | Nightlight | unavailable | area: Office
- binary_sensor.yeelight_ceiling3_0x80355e4_nightlight | Yeelight Ceiling Light (Kids) Nightlight | unavailable | area:
  Kids Rooms

## button (34)

- button.auto_backup_purge_backups | Auto Backup Purge backups | unknown | area: Office
- button.diskstation_reboot | DiskStation Reboot | unknown | area: Office
- button.diskstation_shutdown | DiskStation Shutdown | unknown | area: Office
- button.fritz_box_7590_ax_cleanup | FRITZ!Box 7590 AX Cleanup | unknown | area: Office
- button.fritz_box_7590_ax_firmware_update | FRITZ!Box 7590 AX Firmware update | unknown | area: Office
- button.fritz_box_7590_ax_reconnect | FRITZ!Box 7590 AX Reconnect | unknown | area: Office
- button.fritz_box_7590_ax_restart | FRITZ!Box 7590 AX Restart | unknown | area: Office
- button.fritz_repeater_2400_cleanup | FRITZ!Repeater 2400 Cleanup | unknown | area: Living Room
- button.fritz_repeater_2400_firmware_update | FRITZ!Repeater 2400 Firmware update | unknown | area: Living Room
- button.fritz_repeater_2400_reconnect | FRITZ!Repeater 2400 Reconnect | unknown | area: Living Room
- button.fritz_repeater_2400_restart | FRITZ!Repeater 2400 Restart | unknown | area: Living Room
- button.homeassistant_reload | Home Assistant Reload | unknown
- button.homeassistant_restart | Home Assistant Restart | unknown
- button.ignore_all_issues | Repairs Ignore all | unknown
- button.meross_smart_plug_dishwasher_refresh | Meross-Smart-Plug (Dishwasher) Refresh | unknown | area: Kitchen
- button.meross_smart_plug_dishwasher_reload | Meross-Smart-Plug (Dishwasher) Reload | unknown | area: Kitchen
- button.meross_smart_plug_living_room_refresh | Meross-Smart-Plug (Living Room) Refresh | unknown | area: Living Room
- button.meross_smart_plug_living_room_reload | Meross-Smart-Plug (Living Room) Reload | unknown | area: Living Room
- button.meross_smart_plug_refrigerator_refresh | Meross-Smart-Plug (Refrigerator) Refresh | unknown | area: Kitchen
- button.meross_smart_plug_refrigerator_reload | Meross-Smart-Plug (Refrigerator) Reload | unknown | area: Kitchen
- button.roborock_qrevo_pro_clean_living_room | Roborock Qrevo Pro Clean Living Room | unknown | area: Office
- button.roborock_qrevo_pro_full_vacuum | Roborock Qrevo Pro Full Vacuum | unknown | area: Office
- button.roborock_qrevo_pro_refresh | Roborock Qrevo Pro Refresh | unknown | area: Office
- button.roborock_qrevo_pro_reload | Roborock Qrevo Pro Reload | unknown | area: Office
- button.shellyplugsg3_28372f2f1e04_reboot | Shelly Plug S (E-Bike) Reboot | unknown | area: Office
- button.shellyplusplugs_d4d4da363900_reboot | Shelly Plug S (Office) Reboot | unknown | area: Office
- button.shellypmminig3_dcda0ce9c28c_reboot | Shelly PM Mini Gen3 (Balcony) Reboot | unknown | area: Balcony
- button.shellypro3em_08f9e0e88160_reboot | Shelly Pro 3EM Reboot | unknown | area: Office
- button.smart_plug_19011801871415251h0334298f1a2070_refresh | Washing Machine Refresh | unknown | area: Bathroom
- button.smart_plug_19011801871415251h0334298f1a2070_reload | Washing Machine Reload | unknown | area: Bathroom
- button.smart_plug_1908218495823925185548e1e9023052_refresh | Living room lamp Refresh | unknown | area: Living Room
- button.smart_plug_1908218495823925185548e1e9023052_reload | Living room lamp Reload | unknown | area: Living Room
- button.somfy_tahoma_switch_identify | Somfy TaHoma switch Identify | unavailable | area: Living Room
- button.unignore_all_issues | Repairs Unignore all | unknown

# conversation (1)

- conversation.home_assistant | Home Assistant | unknown

## device_tracker (85)

- device_tracker.35ad9eac_4306_4302_90e3_9930ecaa7be6 | 5421fd6e-7306-4d48-8394-6c0b0d6c1870 | unavailable
- device_tracker.appletv4k | appletv4k | home | area: Living Room
- device_tracker.be1lf209 | BE1LF209 | unavailable
- device_tracker.brothermfc_l2710dw | brothermfc-l2710dw | home | area: Office
- device_tracker.diskstationds918 | diskstationds918 | home | area: Office
- device_tracker.e3e81dda_ae46_46b9_b050_66e5bce85f7d | e3e81dda-ae46-46b9-b050-66e5bce85f7d | unavailable
- device_tracker.echodotkids | echodotkids-hans | not_home | area: Kids Rooms
- device_tracker.fritz_repeater | fritz.repeater | unavailable
- device_tracker.garminfenix7x | garminfenix7x | not_home
- device_tracker.googlepixel6a | googlepixel6a | unavailable
- device_tracker.homeassistant | 2CCF678E8CB3 | home
- device_tracker.homepod | homepod1-livingroom | home
- device_tracker.homepodmini1_office | homepodmini1-office | home
- device_tracker.homepodmini2_office | homepodmini2-office | home
- device_tracker.homepodmini_kitchen | homepodmini-kitchen | home | area: Kitchen
- device_tracker.hoymileshms_800w_2t | hoymileshms-800w-2t | home | area: Balcony
- device_tracker.ipad | iPad | unavailable
- device_tracker.ipadpro | ipadpro | not_home
- device_tracker.iphone | iPhone | unavailable
- device_tracker.iphone12pro | iphone12pro | home
- device_tracker.iphone13_work | iphone13-work | unavailable
- device_tracker.iphone_12_pro | iPhone 12 Pro | home
- device_tracker.iphone_2 | iPhone | unavailable
- device_tracker.iphone_3 | iPhone | unavailable
- device_tracker.iphone_4 | iPhone | unavailable
- device_tracker.iphone_5 | iPhone-XFL7DN71P2 | unavailable
- device_tracker.iphone_6 | iPhone | home
- device_tracker.kindlepaperwhite | kindlepaperwhite | not_home
- device_tracker.lenovo | Lenovo | unavailable
- device_tracker.living_room | Living-Room | unavailable
- device_tracker.living_room_3 | Living-Room-3 | home
- device_tracker.mac | Mac | unavailable
- device_tracker.mac_2 | Mac | home
- device_tracker.macbookair | MacBookAir | home
- device_tracker.macbookair_dennis | macbookair-dennis | unavailable
- device_tracker.macbookair_kristin | macbookair-kristin | unavailable
- device_tracker.macbookpro | MacBookPro | home
- device_tracker.macbookpro14_work | macbookpro14-work | unavailable | area: Office
- device_tracker.macbookpro14_work_2 | macbookpro14-work | home | area: Office
- device_tracker.macbookpro16 | macbookpro16 | unavailable | area: Office
- device_tracker.meross_smart_plug | meross-smart-plug-refrigerator | home | area: Kitchen
- device_tracker.meross_smart_plug_2 | meross-smart-plug-dishwasher | home | area: Kitchen
- device_tracker.meross_smart_plug_3 | Meross-Smart-Plug | home | area: Living Room
- device_tracker.meross_smart_plug_laundry | meross-smart-plug-laundry | home | area: Office
- device_tracker.meross_smart_plug_livingroom | meross-smart-plug-livingroom | home | area: Living Room
- device_tracker.meross_smart_plug_office | meross-smart-plug-office | home | area: Bathroom
- device_tracker.mileddesklamp1s | mileddesklamp1s | home | area: Office
- device_tracker.netatmosmarthomeweatherstation | netatmosmarthomeweatherstation | home
- device_tracker.none_2 | echodotkids-vicky | home
- device_tracker.pc_00_24_e4_4b_f9_10 | PC-00-24-E4-4B-F9-10 | unavailable
- device_tracker.pc_18e6_c2f3_c544_2770 | homepod2-livingroom | not_home
- device_tracker.pc_192_168_178_125 | PC-A4-7E-FA-07-2B-82 | not_home
- device_tracker.pc_192_168_178_74 | iPhone | unavailable
- device_tracker.pc_192_168_178_78 | PC-192-168-178-78 | unavailable
- device_tracker.pc_192_168_178_79 | PC-192-168-178-79 | unavailable
- device_tracker.pc_192_168_178_93 | PC-192-168-178-93 | unavailable
- device_tracker.pc_62_ab_eb_2e_bd_76 | iPhone | home
- device_tracker.pc_7a_94_d2_d1_01_80 | PC-7A-94-D2-D1-01-80 | unavailable
- device_tracker.pc_7a_9f_4b_0f_87_84 | Watch | not_home
- device_tracker.pc_b6_89_c2_97_56_30 | iPad | unavailable
- device_tracker.raspberrypi | homeassistant | unavailable
- device_tracker.raspberrypi4 | raspberrypi4 | unavailable
- device_tracker.rdde01rn | RDDE01RN | unavailable
- device_tracker.roborock_vacuum_a101 | roborockqrevopro | home | area: Office
- device_tracker.roborockq7max | roborockq7max | unavailable | area: Office
- device_tracker.s1b685d4cf11d0aabc_4351 | s1b685d4cf11d0aabc 4351 | unavailable
- device_tracker.s375b78d94b29e41cc_7608 | s375b78d94b29e41cc 7608 | unavailable
- device_tracker.s5969be95236e9382c_61d3 | s5969be95236e9382c 61d3 | unavailable
- device_tracker.samsunggalaxys7 | samsunggalaxys7 | home
- device_tracker.shellyplugsg3_28372f2f1e04 | shellyplugs-ebike | home | area: Office
- device_tracker.shellyplusplugs_d4d4da363900 | shellyplugs-office | home | area: Office
- device_tracker.shellypmminigen3_balcony | shellypmminigen3-balcony | home | area: Balcony
- device_tracker.shellypro3em_08f9e0e88160 | shellypro3em | home
- device_tracker.shellypro3em_08f9e0e88160_2 | Shelly Pro 3EM | unavailable | area: Office
- device_tracker.stades_ipad | Stade’s iPad | home
- device_tracker.toniebox | Toniebox | not_home | area: Kids Rooms
- device_tracker.watch | Watch | unavailable
- device_tracker.watch_2 | Watch | unavailable
- device_tracker.withingsbodycardio | withingsbodycardio | not_home | area: Bedroom
- device_tracker.wsc513101001578 | WSC513101001578 | unavailable
- device_tracker.yeelightceilinglight_diningroom | yeelightceilinglight-diningroom | not_home
- device_tracker.yeelightceilinglight_hans | yeelightceilinglight-hans | not_home
- device_tracker.yeelightceilinglight_livingroom | yeelightceilinglight-livingroom | not_home
- device_tracker.yeelightceilinglight_office | yeelightceilinglight-office | not_home
- device_tracker.yeelink_light_ceiling11_miiof2 | yeelightceilinglight-bedroom | not_home

## event (2)

- event.backup_automatic_backup | Backup Automatic backup | 2025-10-20T03:05:52.147+00:00
- event.repair | Repairs | 2025-10-20T10:11:57.502+00:00

## image (3)

- image.fritz_box_7590_ax_fritz_box_gastzugang | FRITZ!Box 7590 AX FRITZ!Box Gastzugang | 2025-10-19T19:13:13.800866+00:
  00 | area: Office
- image.fritz_repeater_2400_fritz_box_gastzugang | FRITZ!Repeater 2400 FRITZ!Box Gastzugang | 2025-10-19T19:13:
  13.123320+00:00 | area: Living Room
- image.roborock_qrevo_pro_map_0 | Roborock Qrevo Pro Map 0 | 2025-10-19T19:12:40.996251+00:00 | area: Office

## input_boolean (8)

- input_boolean.dishwasher_running | Dishwasher Running | off
- input_boolean.ebike_block_peak | Block charging during peak | off
- input_boolean.ebike_offpeak_backup | Allow off-peak backup charging | off
- input_boolean.kids_room_co2_high_alert | Kids Room CO2 High Alert | off
- input_boolean.laundry_running | Laundry Running | off
- input_boolean.living_room_co2_high_alert | Living Room CO2 High Alert | on
- input_boolean.office_co2_high_alert | Office CO2 High Alert | on
- input_boolean.solar_export_notified_today | Solar Export Notified Today | on

## input_datetime (2)

- input_datetime.ebike_last_off | Ebike last OFF | 2025-10-20 04:06:21
- input_datetime.ebike_last_on | Ebike last ON | 2025-10-20 12:23:35

## input_number (8)

- input_number.ebike_charger_watts | Charger watts | 150.0
- input_number.ebike_daily_target_minutes | Daily target charge (min) | 120.0
- input_number.ebike_min_charge_min | Minimum charge run (min) | 10.0
- input_number.ebike_min_pause_min | Minimum pause time (min) | 10.0
- input_number.ebike_start_dwell_min | Start dwell (min) | 3.0
- input_number.ebike_start_threshold_w | Start export threshold (W) | 200.0 W
- input_number.ebike_stop_dwell_min | Stop dwell (min) | 2.0
- input_number.ebike_stop_threshold_w | Stop export threshold (W) | 100.0 W

## input_select (1)

- input_select.ebike_charge_state | Ebike Charge State | charging

## light (14)

- light.meross_smart_plug_living_room_dnd | Meross-Smart-Plug (Living Room) Dnd | on | area: Living Room
- light.smart_plug_19011801871415251h0334298f1a2070_dnd | Washing Machine Dnd | off | area: Bathroom
- light.smart_plug_1908212877531725185548e1e90233ca_dnd | Meross-Smart-Plug (Dishwasher) Dnd | on | area: Kitchen
- light.smart_plug_1908213017294825185548e1e9024169_dnd | Meross-Smart-Plug (Refrigerator) Dnd | on | area: Kitchen
- light.smart_plug_1908215645566225185548e1e9023170_dnd | Roborock Qrevo Pro Dnd | off | area: Office
- light.smart_plug_1908218495823925185548e1e9023052_dnd | Living room lamp Dnd | off | area: Living Room
- light.yeelight_ceilc_0x178697e2 | Yeelight Living Room | unavailable | area: Living Room
- light.yeelight_ceilc_0x178697e2_ambilight | Yeelight Living Room Ambilight | unavailable | area: Living Room
- light.yeelight_ceilc_0x1786992c | Yeelight Dining Room | unavailable | area: Living Room
- light.yeelight_ceilc_0x1786992c_ambilight | Yeelight Dining Room Ambilight | unavailable | area: Living Room
- light.yeelight_ceiling11_0x101c56f2 | Yeelight Ceiling Light (Bed Room) | unavailable | area: Bedroom
- light.yeelight_ceiling11_0x66a47e6 | yeelight ceiling11 0x66a47e6 | unavailable | area: Office
- light.yeelight_ceiling3_0x80355e4 | Yeelight Ceiling Light (Kids) | unavailable | area: Kids Rooms
- light.yeelight_color_0x7de176c | yeelight color 0x7de176c | unavailable | area: Living Room

## media_player (6)

- media_player.kitchen | HomePod mini (Kitchen) | off | area: Kitchen
- media_player.living_room | Living Room | off | area: Living Room
- media_player.living_room_2 | HomePod (Living Room) | off | area: Living Room
- media_player.living_room_3 | HomePod (Living Room) | off | area: Living Room
- media_player.office_2 | HomePod Mini (Office) | off | area: Office
- media_player.office_3 | HomePod Mini (Office) | off | area: Office

## number (1)

- number.roborock_qrevo_pro_volume | Roborock Qrevo Pro Volume | 90 % | area: Office

## person (2)

- person.christian_stade_schuldt | Christian Stade-Schuldt | home
- person.kristin_kopernik | Kristin Köpernik | unknown

## remote (6)

- remote.kitchen | Apple HomePod mini (HomePod mini (Kitchen)) | off | area: Kitchen
- remote.living_room | Living Room | on | area: Living Room
- remote.living_room_2 | HomePod (Living Room) | on | area: Living Room
- remote.living_room_3 | HomePod (Living Room) | on | area: Living Room
- remote.office_2 | HomePod Mini (Office) | off | area: Office
- remote.office_3 | HomePod Mini (Office) | off | area: Office

## schedule (2)

- schedule.ebike_offpeak | Ebike Offpeak Charging | off | area: Office
- schedule.peak_demand | Peak Demand | off | area: Office

## select (5)

- select.roborock_qrevo_pro_dock_empty_mode | Roborock Qrevo Pro Dock Empty mode | max | area: Office
- select.roborock_qrevo_pro_mop_intensity | Roborock Qrevo Pro Mop intensity | medium | area: Office
- select.roborock_qrevo_pro_mop_mode | Roborock Qrevo Pro Mop mode | standard | area: Office
- select.roborock_qrevo_pro_selected_map | Roborock Qrevo Pro Selected map | Map 0 | area: Office
- select.solcast_pv_forecast_use_forecast_field | Solcast PV Forecast Use Forecast Field | estimate | area: Balcony

## sensor (340)

- sensor.active_issues | Repairs Active | 0 issues
- sensor.air_quality | Home Assistant Air quality | 0
- sensor.alarm_control_panels | Home Assistant Alarm control panels | 0
- sensor.areas | Home Assistant Areas | 8
- sensor.auto_backup | Auto Backup | 0 pending backup(s) | area: Office
- sensor.auto_backup_last_failure | Auto Backup Last failure | unknown | area: Office
- sensor.auto_backup_last_success | Auto Backup Last success | unknown | area: Office
- sensor.auto_backup_monitored_backups | Auto Backup Monitored backups | 0 | area: Office
- sensor.auto_backup_purgeable_backups | Auto Backup Purgeable backups | 0 | area: Office
- sensor.automations | Home Assistant Automations | 45
- sensor.backup_backup_manager_state | Backup Backup Manager state | idle
- sensor.backup_last_attempted_automatic_backup | Backup Last attempted automatic backup | 2025-10-20T03:05:26+00:00
- sensor.backup_last_successful_automatic_backup | Backup Last successful automatic backup | 2025-10-20T03:05:51+00:00
- sensor.backup_next_scheduled_automatic_backup | Backup Next scheduled automatic backup | 2025-10-21T03:43:19+00:00
- sensor.binary_sensors | Home Assistant Binary sensors | 47
- sensor.brother_mfc_l2710dw_series | Brother MFC-L2710DW series | idle | area: Office
- sensor.brother_mfc_l2710dw_series_bk | Brother MFC-L2710DW series BK | 100 % | area: Office
- sensor.buttons | Home Assistant Buttons | 34
- sensor.calendars | Home Assistant Calendars | 0
- sensor.cameras | Home Assistant Cameras | 0
- sensor.climate | Home Assistant Climate | 0
- sensor.covers | Home Assistant Covers | 0
- sensor.custom_integrations | Home Assistant Custom integrations | 7
- sensor.daily_grid_export | Daily Grid Export | 1.00759 kWh | area: Office
- sensor.daily_grid_import | Daily Grid Import | 4.41258 kWh | area: Office
- sensor.daily_solar_production | Daily Solar Production | 1.639525 kWh | area: Balcony
- sensor.dates | Home Assistant Dates | 0
- sensor.datetimes | Home Assistant Date/times | 0
- sensor.device_trackers | Home Assistant Device trackers | 85
- sensor.devices | Home Assistant Devices | 154
- sensor.dishwasher_phase | Dishwasher phase | idle
- sensor.diskstation_cache_device_1_status | DiskStation (Cache device 1) Status | normal | area: Office
- sensor.diskstation_cache_device_1_temperature | DiskStation (Cache device 1) Temperature | 45 °C | area: Office
- sensor.diskstation_cache_device_2_status | DiskStation (Cache device 2) Status | normal | area: Office
- sensor.diskstation_cache_device_2_temperature | DiskStation (Cache device 2) Temperature | 44 °C | area: Office
- sensor.diskstation_cpu_load_average_15_min | DiskStation CPU load average (15 min) | 0.14 load | area: Office
- sensor.diskstation_cpu_load_average_5_min | DiskStation CPU load average (5 min) | 0.02 load | area: Office
- sensor.diskstation_cpu_utilization_total | DiskStation CPU utilization (total) | 2 % | area: Office
- sensor.diskstation_cpu_utilization_user | DiskStation CPU utilization (user) | 0 % | area: Office
- sensor.diskstation_download_throughput | DiskStation Download throughput | 1.238 kB/s | area: Office
- sensor.diskstation_drive_1_status | DiskStation (Drive 1) Status | normal | area: Office
- sensor.diskstation_drive_1_temperature | DiskStation (Drive 1) Temperature | 42 °C | area: Office
- sensor.diskstation_drive_2_status | DiskStation (Drive 2) Status | normal | area: Office
- sensor.diskstation_drive_2_temperature | DiskStation (Drive 2) Temperature | 43 °C | area: Office
- sensor.diskstation_drive_3_status | DiskStation (Drive 3) Status | normal | area: Office
- sensor.diskstation_drive_3_temperature | DiskStation (Drive 3) Temperature | 43 °C | area: Office
- sensor.diskstation_drive_4_status | DiskStation (Drive 4) Status | normal | area: Office
- sensor.diskstation_drive_4_temperature | DiskStation (Drive 4) Temperature | 41 °C | area: Office
- sensor.diskstation_memory_available_real | DiskStation Memory available (real) | 1529.696256 MB | area: Office
- sensor.diskstation_memory_available_swap | DiskStation Memory available (swap) | 6148.145152 MB | area: Office
- sensor.diskstation_memory_total_real | DiskStation Memory total (real) | 8181.00224 MB | area: Office
- sensor.diskstation_memory_total_swap | DiskStation Memory total (swap) | 7058.927616 MB | area: Office
- sensor.diskstation_memory_usage_real | DiskStation Memory usage (real) | 21 % | area: Office
- sensor.diskstation_temperature | DiskStation Temperature | 50 °C | area: Office
- sensor.diskstation_upload_throughput | DiskStation Upload throughput | 0.164 kB/s | area: Office
- sensor.diskstation_volume_1_average_disk_temp | DiskStation (Volume 1) Average disk temp | 42.0 °C | area: Office
- sensor.diskstation_volume_1_status | DiskStation (Volume 1) Status | normal | area: Office
- sensor.diskstation_volume_1_used_space | DiskStation (Volume 1) Used space | 6.770933956608 TB | area: Office
- sensor.diskstation_volume_1_volume_used | DiskStation (Volume 1) Volume used | 35.3 % | area: Office
- sensor.ebike_charging_hours_today_raw | Ebike Charging Hours Today Raw | 0.47 h
- sensor.ebike_charging_minutes_today | Ebike Charging Minutes Today | 28 min
- sensor.ebike_estimated_energy_today | Ebike Estimated Energy Today | 70 Wh
- sensor.entities | Home Assistant Entities | 751
- sensor.excess_solar_export | Excess Solar Export | 150 W
- sensor.fans | Home Assistant Fans | 0
- sensor.fridge_battery | Fridge | 64 % | area: Kitchen
- sensor.fridge_humidity | Fridge | 44.7 % | area: Kitchen
- sensor.fridge_temperature | Fridge | 7.9 °C | area: Kitchen
- sensor.fridge_voltage | Fridge | 2.776 V | area: Kitchen
- sensor.fritz_box_7590_ax_connection_uptime | FRITZ!Box 7590 AX Connection uptime | 2025-10-13T00:05:07+00:00 | area:
  Office
- sensor.fritz_box_7590_ax_cpu_temperature | FRITZ!Box 7590 AX CPU temperature | 84 °C | area: Office
- sensor.fritz_box_7590_ax_download_speed | FRITZ!Box 7590 AX Download speed | 7.01082413605904 KiB/s | area: Office
- sensor.fritz_box_7590_ax_download_speed_2 | FRITZ!Box 7590 AX Download speed | 7.00013078725205 KiB/s | area: Office
- sensor.fritz_box_7590_ax_download_throughput | FRITZ!Box 7590 AX Download throughput | 3.8 kB/s | area: Office
- sensor.fritz_box_7590_ax_external_ip | FRITZ!Box 7590 AX External IP | 217.94.244.135 | area: Office
- sensor.fritz_box_7590_ax_external_ip_2 | FRITZ!Box 7590 AX External IP | 217.94.244.135 | area: Office
- sensor.fritz_box_7590_ax_external_ip_3 | FRITZ!Box 7590 AX External IP | 217.94.244.135 | area: Office
- sensor.fritz_box_7590_ax_external_ipv6 | FRITZ!Box 7590 AX External IPv6 | 2003:d4:6fff:1e53:4a5d:35ff:fe15:27f3 |
  area: Office
- sensor.fritz_box_7590_ax_gb_received | FRITZ!Box 7590 AX GB received | 95.4 GB | area: Office
- sensor.fritz_box_7590_ax_gb_sent | FRITZ!Box 7590 AX GB sent | 13.5 GB | area: Office
- sensor.fritz_box_7590_ax_last_restart | FRITZ!Box 7590 AX Last restart | 2025-10-13T00:01:22+00:00 | area: Office
- sensor.fritz_box_7590_ax_link_download_noise_margin | FRITZ!Box 7590 AX Link download noise margin | 11.0 dB | area:
  Office
- sensor.fritz_box_7590_ax_link_download_power_attenuation | FRITZ!Box 7590 AX Link download power attenuation | 9.0
  dB | area: Office
- sensor.fritz_box_7590_ax_link_download_throughput | FRITZ!Box 7590 AX Link download throughput | 134788.0 kbit/s |
  area: Office
- sensor.fritz_box_7590_ax_link_upload_noise_margin | FRITZ!Box 7590 AX Link upload noise margin | 9.0 dB | area: Office
- sensor.fritz_box_7590_ax_link_upload_power_attenuation | FRITZ!Box 7590 AX Link upload power attenuation | 6.0 dB |
  area: Office
- sensor.fritz_box_7590_ax_link_upload_throughput | FRITZ!Box 7590 AX Link upload throughput | 52232.0 kbit/s | area:
  Office
- sensor.fritz_box_7590_ax_max_connection_download_throughput | FRITZ!Box 7590 AX Max connection download throughput |
  113240.0 kbit/s | area: Office
- sensor.fritz_box_7590_ax_max_connection_upload_throughput | FRITZ!Box 7590 AX Max connection upload throughput |
  45513.0 kbit/s | area: Office
- sensor.fritz_box_7590_ax_upload_speed | FRITZ!Box 7590 AX Upload speed | 4.73581437487175 KiB/s | area: Office
- sensor.fritz_box_7590_ax_upload_speed_2 | FRITZ!Box 7590 AX Upload speed | 4.68320374179251 KiB/s | area: Office
- sensor.fritz_box_7590_ax_upload_throughput | FRITZ!Box 7590 AX Upload throughput | 4.0 kB/s | area: Office
- sensor.fritz_repeater_2400_cpu_temperature | CPU temperature | unavailable °C | area: Living Room
- sensor.fritz_repeater_2400_last_restart | FRITZ!Repeater 2400 Last restart | unavailable | area: Living Room
- sensor.home | Home | 3.8385 kWh | area: Balcony
- sensor.humidifiers | Home Assistant Humidifiers | 0
- sensor.ignored_issues | Repairs Ignored | 0 issues
- sensor.images | Home Assistant Images | 3
- sensor.input_booleans | Home Assistant Input booleans | 8
- sensor.input_buttons | Home Assistant Input buttons | 0
- sensor.input_datetimes | Home Assistant Input date/times | 2
- sensor.input_numbers | Home Assistant Input numbers | 8
- sensor.input_selects | Home Assistant Input selects | 1
- sensor.input_texts | Home Assistant Input texts | 0
- sensor.integrations | Home Assistant Integrations | 79
- sensor.iphone_12_pro_activity | iPhone 12 Pro Activity | Stationary
- sensor.iphone_12_pro_app_version | iPhone 12 Pro App Version | 2025.10.0
- sensor.iphone_12_pro_audio_output | iPhone 12 Pro Audio Output | Built-in Speaker
- sensor.iphone_12_pro_average_active_pace | iPhone 12 Pro Average Active Pace | 0 m/s
- sensor.iphone_12_pro_battery_level | iPhone 12 Pro Battery Level | 85 %
- sensor.iphone_12_pro_battery_state | iPhone 12 Pro Battery State | Not Charging
- sensor.iphone_12_pro_bssid | iPhone 12 Pro BSSID | 48:5d:35:15:27:f9
- sensor.iphone_12_pro_connection_type | iPhone 12 Pro Connection Type | Wi-Fi
- sensor.iphone_12_pro_distance | iPhone 12 Pro Distance | 2792 m
- sensor.iphone_12_pro_floors_ascended | iPhone 12 Pro Floors Ascended | 10 floors
- sensor.iphone_12_pro_floors_descended | iPhone 12 Pro Floors Descended | 6 floors
- sensor.iphone_12_pro_geocoded_location | iPhone 12 Pro Geocoded Location | Schwiebusser Straße 45
  10965 Berlin
  Germany
- sensor.iphone_12_pro_last_update_trigger | iPhone 12 Pro Last Update Trigger | Background Fetch
- sensor.iphone_12_pro_location_permission | iPhone 12 Pro Location permission | Authorized Always
- sensor.iphone_12_pro_sim_1 | iPhone 12 Pro SIM 1 | --
- sensor.iphone_12_pro_sim_2 | iPhone 12 Pro SIM 2 | --
- sensor.iphone_12_pro_ssid | iPhone 12 Pro SSID | FRITZ!Box 7590 IF
- sensor.iphone_12_pro_steps | iPhone 12 Pro Steps | 4244 steps
- sensor.iphone_12_pro_storage | iPhone 12 Pro Storage | 8.82 % available
- sensor.issues | Repairs Total | 0 issues
- sensor.lights | Home Assistant Lights | 14
- sensor.living_room_station_atmospheric_pressure | Netatmo Living Room Atmospheric pressure | 1006.2 hPa | area: Living
  Room
- sensor.living_room_station_bedroom_battery | Netatmo Bedroom Battery | 43 % | area: Bedroom
- sensor.living_room_station_bedroom_carbon_dioxide | Netatmo Bedroom Carbon dioxide | 932 ppm | area: Bedroom
- sensor.living_room_station_bedroom_humidity | Netatmo Bedroom Humidity | 53 % | area: Bedroom
- sensor.living_room_station_bedroom_temperature | Netatmo Bedroom Temperature | 22.9 °C | area: Bedroom
- sensor.living_room_station_carbon_dioxide | Netatmo Living Room Carbon dioxide | 1019 ppm | area: Living Room
- sensor.living_room_station_hans_battery | Netatmo Hans Battery | 44 % | area: Kids Rooms
- sensor.living_room_station_hans_carbon_dioxide | Netatmo Hans Carbon dioxide | 938 ppm | area: Kids Rooms
- sensor.living_room_station_hans_humidity | Netatmo Hans Humidity | 49 % | area: Kids Rooms
- sensor.living_room_station_hans_temperature | Netatmo Hans Temperature | 23.8 °C | area: Kids Rooms
- sensor.living_room_station_humidity | Netatmo Living Room Humidity | 45 % | area: Living Room
- sensor.living_room_station_noise | Netatmo Living Room Noise | 51 dB | area: Living Room
- sensor.living_room_station_office_battery | Netatmo Office Battery | 46 % | area: Office
- sensor.living_room_station_office_carbon_dioxide | Netatmo Office Carbon dioxide | 1002 ppm | area: Office
- sensor.living_room_station_office_humidity | Netatmo Office Humidity | 45 % | area: Office
- sensor.living_room_station_office_temperature | Netatmo Office Temperature | 23.3 °C | area: Office
- sensor.living_room_station_outdoor_module_battery | Netatmo Balcony Battery | 51 % | area: Balcony
- sensor.living_room_station_outdoor_module_humidity | Netatmo Balcony Humidity | 77 % | area: Balcony
- sensor.living_room_station_outdoor_module_temperature | Netatmo Balcony Temperature | 10.2 °C | area: Balcony
- sensor.living_room_station_rain_gauge_battery | Netatmo Rain Gauge Battery | 93 % | area: Balcony
- sensor.living_room_station_rain_gauge_precipitation | Netatmo Rain Gauge Precipitation | 0 mm | area: Balcony
- sensor.living_room_station_rain_gauge_precipitation_today | Netatmo Rain Gauge Precipitation today | 0 mm | area:
  Balcony
- sensor.living_room_station_smart_anemometer_battery | Netatmo Anemometer Battery | 46 % | area: Balcony
- sensor.living_room_station_smart_anemometer_wind_direction | Netatmo Anemometer Wind direction | w | area: Balcony
- sensor.living_room_station_smart_anemometer_wind_speed | Netatmo Anemometer Wind speed | 2 km/h | area: Balcony
- sensor.living_room_station_temperature | Netatmo Living Room Temperature | 24.2 °C | area: Living Room
- sensor.locks | Home Assistant Locks | 0
- sensor.media_players | Home Assistant Media players | 6
- sensor.meross_smart_plug_living_room_config_overtemp_type | Meross-Smart-Plug (Living Room) Config overtemp type | 1 |
  area: Living Room
- sensor.meross_smart_plug_living_room_consumption | Meross-Smart-Plug (Living Room) Consumption | 125.0 Wh | area:
  Living Room
- sensor.meross_smart_plug_living_room_current | Meross-Smart-Plug (Living Room) Current | 0.134 A | area: Living Room
- sensor.meross_smart_plug_living_room_energy | Meross-Smart-Plug (Living Room) Energy | 125 Wh | area: Living Room
- sensor.meross_smart_plug_living_room_power | Meross-Smart-Plug (Living Room) Power | 10.576 W | area: Living Room
- sensor.meross_smart_plug_living_room_signal_strength | Meross-Smart-Plug (Living Room) Signal strength | 100 % | area:
  Living Room
- sensor.meross_smart_plug_living_room_voltage | Meross-Smart-Plug (Living Room) Voltage | 229.3 V | area: Living Room
- sensor.mfc_l2710dw_black_toner_remaining | MFC-L2710DW Black toner remaining | 91 % | area: Office
- sensor.mfc_l2710dw_drum_page_counter | MFC-L2710DW Drum page counter | 2136 pages | area: Office
- sensor.mfc_l2710dw_drum_remaining_lifetime | MFC-L2710DW Drum remaining lifetime | 83 % | area: Office
- sensor.mfc_l2710dw_drum_remaining_pages | MFC-L2710DW Drum remaining pages | 9864 pages | area: Office
- sensor.mfc_l2710dw_duplex_unit_page_counter | MFC-L2710DW Duplex unit page counter | 796 pages | area: Office
- sensor.mfc_l2710dw_page_counter | MFC-L2710DW Page counter | 2136 pages | area: Office
- sensor.mfc_l2710dw_status | MFC-L2710DW Status | energiesparen | area: Office
- sensor.monthly_grid_export | Monthly Grid Export | 16.84779 kWh | area: Office
- sensor.monthly_grid_import | Monthly Grid Import | 155.15352 kWh | area: Office
- sensor.monthly_self_consumed_solar_energy | Monthly Self Consumed Solar Energy | 9.05 kWh
- sensor.monthly_solar_production | Monthly Solar Production | 25.898288 kWh | area: Balcony
- sensor.numbers | Home Assistant Numbers | 1
- sensor.openweathermap_cloud_coverage | OpenWeatherMap Cloud coverage | 0 % | area: Balcony
- sensor.openweathermap_condition | OpenWeatherMap Condition | sunny | area: Balcony
- sensor.openweathermap_dew_point | OpenWeatherMap Dew Point | unknown °C | area: Balcony
- sensor.openweathermap_feels_like_temperature | OpenWeatherMap Feels like temperature | 10.25 °C | area: Balcony
- sensor.openweathermap_humidity | OpenWeatherMap Humidity | 66 % | area: Balcony
- sensor.openweathermap_precipitation_kind | OpenWeatherMap Precipitation kind | None | area: Balcony
- sensor.openweathermap_pressure | OpenWeatherMap Pressure | 1007 hPa | area: Balcony
- sensor.openweathermap_rain | OpenWeatherMap Rain | 0 mm/h | area: Balcony
- sensor.openweathermap_snow | OpenWeatherMap Snow | 0 mm/h | area: Balcony
- sensor.openweathermap_temperature | OpenWeatherMap Temperature | 11.34 °C | area: Balcony
- sensor.openweathermap_uv_index | OpenWeatherMap UV Index | unknown UV index | area: Balcony
- sensor.openweathermap_visibility | OpenWeatherMap Visibility | 10000 m | area: Balcony
- sensor.openweathermap_weather | OpenWeatherMap Weather | clear sky | area: Balcony
- sensor.openweathermap_weather_code | OpenWeatherMap Weather Code | 800 | area: Balcony
- sensor.openweathermap_wind_bearing | OpenWeatherMap Wind bearing | 124 ° | area: Balcony
- sensor.openweathermap_wind_gust | OpenWeatherMap Wind gust | 35.388 km/h | area: Balcony
- sensor.openweathermap_wind_speed | OpenWeatherMap Wind speed | 24.156 km/h | area: Balcony
- sensor.persistent_notifications | Home Assistant Persistent notifications | 0
- sensor.persons | Home Assistant Persons | 2
- sensor.remotes | Home Assistant Remotes | 6
- sensor.roborock_qrevo_pro_battery | Roborock Qrevo Pro Battery | 100 % | area: Office
- sensor.roborock_qrevo_pro_cleaning_area | Roborock Qrevo Pro Cleaning area | 72.1 m² | area: Office
- sensor.roborock_qrevo_pro_cleaning_progress | Roborock Qrevo Pro Cleaning progress | 0 % | area: Office
- sensor.roborock_qrevo_pro_cleaning_time | Roborock Qrevo Pro Cleaning time | 5347 s | area: Office
- sensor.roborock_qrevo_pro_current_room | Roborock Qrevo Pro Current room | Study | area: Office
- sensor.roborock_qrevo_pro_dock_dock_error | Roborock Qrevo Pro Dock Dock error | water_empty | area: Office
- sensor.roborock_qrevo_pro_dock_mop_drying_remaining_time | Roborock Qrevo Pro Dock Mop drying remaining time | 0 s |
  area: Office
- sensor.roborock_qrevo_pro_filter_time_left | Roborock Qrevo Pro Filter time left | 74208 s | area: Office
- sensor.roborock_qrevo_pro_last_clean_begin | Roborock Qrevo Pro Last clean begin | 2025-10-19T14:17:55+00:00 | area:
  Office
- sensor.roborock_qrevo_pro_last_clean_end | Roborock Qrevo Pro Last clean end | 2025-10-19T15:47:06+00:00 | area:
  Office
- sensor.roborock_qrevo_pro_main_brush_time_left | Roborock Qrevo Pro Main brush time left | 614208 s | area: Office
- sensor.roborock_qrevo_pro_sensor_time_left | Roborock Qrevo Pro Sensor time left | 88657 s | area: Office
- sensor.roborock_qrevo_pro_side_brush_time_left | Roborock Qrevo Pro Side brush time left | 254208 s | area: Office
- sensor.roborock_qrevo_pro_status | Roborock Qrevo Pro Status | charging | area: Office
- sensor.roborock_qrevo_pro_total_cleaning_area | Roborock Qrevo Pro Total cleaning area | 6174.2 m² | area: Office
- sensor.roborock_qrevo_pro_total_cleaning_count | Roborock Qrevo Pro Total cleaning count | 143 | area: Office
- sensor.roborock_qrevo_pro_total_cleaning_time | Roborock Qrevo Pro Total cleaning time | 465792 s | area: Office
- sensor.roborock_qrevo_pro_vacuum_error | Roborock Qrevo Pro Vacuum error | none | area: Office
- sensor.s1b685d4cf11d0aabc_4351_estimated_distance | Estimated distance | unavailable m
- sensor.s375b78d94b29e41cc_7608_estimated_distance | Estimated distance | unavailable m
- sensor.s5969be95236e9382c_61d3_estimated_distance | Estimated distance | unavailable m
- sensor.scenes | Home Assistant Scenes | 0
- sensor.scripts | Home Assistant Scripts | 0
- sensor.selects | Home Assistant Selects | 5
- sensor.self_consumed_solar_energy_today | Self Consumed Solar Energy Today | 0.631935 kWh
- sensor.sensors | Home Assistant Sensors | 340
- sensor.shellyplugsg3_28372f2f1e04_energy | Shelly Plug S (E-Bike) Total energy | 7.256389 kWh | area: Office
- sensor.shellyplugsg3_28372f2f1e04_power | Shelly Plug S (E-Bike) Power | 190.8 W | area: Office
- sensor.shellyplusplugs_d4d4da363900_energy | Shelly Plug S (Office) Total energy | 86.359073 kWh | area: Office
- sensor.shellyplusplugs_d4d4da363900_power | Shelly Plug S (Office) Power | 43.5 W | area: Office
- sensor.shellypmminig3_dcda0ce9c28c_energy | Shelly PM Mini Gen3 (Balcony) energy | 810.451716 kWh | area: Balcony
- sensor.shellypmminig3_dcda0ce9c28c_power | Shelly PM Mini Gen3 (Balcony) power | -504.3 W | area: Balcony
- sensor.shellypro3em_08f9e0e88160_phase_a_active_power | Shelly Pro 3EM phase a active power | 342.8 W | area: Office
- sensor.shellypro3em_08f9e0e88160_phase_a_apparent_power | Shelly Pro 3EM phase a apparent power | 465.8 VA | area:
  Office
- sensor.shellypro3em_08f9e0e88160_phase_a_power_factor | Shelly Pro 3EM phase a power factor | 0.74 | area: Office
- sensor.shellypro3em_08f9e0e88160_phase_b_active_power | Shelly Pro 3EM phase b active power | -491.4 W | area: Office
- sensor.shellypro3em_08f9e0e88160_phase_b_apparent_power | Shelly Pro 3EM phase b apparent power | 493.6 VA | area:
  Office
- sensor.shellypro3em_08f9e0e88160_phase_b_power_factor | Shelly Pro 3EM phase b power factor | 0.99 | area: Office
- sensor.shellypro3em_08f9e0e88160_phase_c_active_power | Shelly Pro 3EM phase c active power | -1.4 W | area: Office
- sensor.shellypro3em_08f9e0e88160_phase_c_apparent_power | Shelly Pro 3EM phase c apparent power | 29.8 VA | area:
  Office
- sensor.shellypro3em_08f9e0e88160_phase_c_power_factor | Shelly Pro 3EM phase c power factor | 0.04 | area: Office
- sensor.shellypro3em_08f9e0e88160_temperature | Shelly Pro 3EM temperature | 47.0 °C | area: Office
- sensor.shellypro3em_08f9e0e88160_total_active_energy | Shelly Pro 3EM total active energy | 2561.51589 kWh | area:
  Office
- sensor.shellypro3em_08f9e0e88160_total_active_energy_cost | sensor Cost | 1.70130068999999 EUR
- sensor.shellypro3em_08f9e0e88160_total_active_power | Shelly Pro 3EM total active power | -150.058 W | area: Office
- sensor.shellypro3em_08f9e0e88160_total_active_returned_energy | Shelly Pro 3EM total active returned energy |
  443.19849 kWh | area: Office
- sensor.shellypro3em_08f9e0e88160_total_apparent_power | Shelly Pro 3EM total apparent power | 989.186 VA | area:
  Office
- sensor.sirens | Home Assistant Sirens | 0
- sensor.smart_plug_19011801871415251h0334298f1a2070_current | Washing Machine Current | 0.0 A | area: Bathroom
- sensor.smart_plug_19011801871415251h0334298f1a2070_energy | Washing Machine Energy | 1360 Wh | area: Bathroom
- sensor.smart_plug_19011801871415251h0334298f1a2070_power | Washing Machine Power | 0.0 W | area: Bathroom
- sensor.smart_plug_19011801871415251h0334298f1a2070_signal_strength | Washing Machine Signal strength | 47 % | area:
  Bathroom
- sensor.smart_plug_19011801871415251h0334298f1a2070_voltage | Washing Machine Voltage | 225.6 V | area: Bathroom
- sensor.smart_plug_1908212877531725185548e1e90233ca_current | Meross-Smart-Plug (Dishwasher) Current | 0.05 A | area:
  Kitchen
- sensor.smart_plug_1908212877531725185548e1e90233ca_energy | Meross-Smart-Plug (Dishwasher) Energy | 752 Wh | area:
  Kitchen
- sensor.smart_plug_1908212877531725185548e1e90233ca_power | Meross-Smart-Plug (Dishwasher) Power | 3.214 W | area:
  Kitchen
- sensor.smart_plug_1908212877531725185548e1e90233ca_signal_strength | Meross-Smart-Plug (Dishwasher) Signal strength |
  50 % | area: Kitchen
- sensor.smart_plug_1908212877531725185548e1e90233ca_voltage | Meross-Smart-Plug (Dishwasher) Voltage | 229.3 V | area:
  Kitchen
- sensor.smart_plug_1908213017294825185548e1e9024169_current | Meross-Smart-Plug (Refrigerator) Current | 0.034 A |
  area: Kitchen
- sensor.smart_plug_1908213017294825185548e1e9024169_energy | Meross-Smart-Plug (Refrigerator) Energy | 526 Wh | area:
  Kitchen
- sensor.smart_plug_1908213017294825185548e1e9024169_power | Meross-Smart-Plug (Refrigerator) Power | 0.789 W | area:
  Kitchen
- sensor.smart_plug_1908213017294825185548e1e9024169_signal_strength | Meross-Smart-Plug (Refrigerator) Signal
  strength | 65 % | area: Kitchen
- sensor.smart_plug_1908213017294825185548e1e9024169_voltage | Meross-Smart-Plug (Refrigerator) Voltage | 229.3 V |
  area: Kitchen
- sensor.smart_plug_1908215645566225185548e1e9023170_current | Roborock Qrevo Pro Current | 0.099 A | area: Office
- sensor.smart_plug_1908215645566225185548e1e9023170_energy | Roborock Qrevo Pro Energy | 36 Wh | area: Office
- sensor.smart_plug_1908215645566225185548e1e9023170_power | Roborock Qrevo Pro Power | 2.65 W | area: Office
- sensor.smart_plug_1908215645566225185548e1e9023170_signal_strength | Roborock Qrevo Pro Signal strength | 100 % |
  area: Office
- sensor.smart_plug_1908215645566225185548e1e9023170_voltage | Roborock Qrevo Pro Voltage | 229.3 V | area: Office
- sensor.smart_plug_1908218495823925185548e1e9023052_current | Living room lamp Current | 0.0 A | area: Living Room
- sensor.smart_plug_1908218495823925185548e1e9023052_energy | Living room lamp Energy | 0 Wh | area: Living Room
- sensor.smart_plug_1908218495823925185548e1e9023052_power | Living room lamp Power | 0.0 W | area: Living Room
- sensor.smart_plug_1908218495823925185548e1e9023052_signal_strength | Living room lamp Signal strength | 73 % | area:
  Living Room
- sensor.smart_plug_1908218495823925185548e1e9023052_voltage | Living room lamp Voltage | 231.2 V | area: Living Room
- sensor.solcast_pv_forecast_api_last_polled | Solcast PV Forecast API Last Polled | 2025-10-20T10:50:44+00:00 | area:
  Balcony
- sensor.solcast_pv_forecast_api_limit | Solcast PV Forecast API Limit | 10 | area: Balcony
- sensor.solcast_pv_forecast_api_used | Solcast PV Forecast API Used | 4 | area: Balcony
- sensor.solcast_pv_forecast_forecast_next_hour | Solcast PV Forecast Forecast Next Hour | 589 Wh | area: Balcony
- sensor.solcast_pv_forecast_forecast_remaining_today | Solcast PV Forecast Forecast Remaining Today | 1.7486 kWh |
  area: Balcony
- sensor.solcast_pv_forecast_forecast_this_hour | Solcast PV Forecast Forecast This Hour | 670 Wh | area: Balcony
- sensor.solcast_pv_forecast_forecast_today | Solcast PV Forecast Forecast Today | 3.8385 kWh | area: Balcony
- sensor.solcast_pv_forecast_forecast_tomorrow | Solcast PV Forecast Forecast Tomorrow | 2.4427 kWh | area: Balcony
- sensor.solcast_pv_forecast_hard_limit_set | Solcast PV Forecast Hard Limit Set | False | area: Balcony
- sensor.solcast_pv_forecast_peak_forecast_today | Solcast PV Forecast Peak Forecast Today | 672 W | area: Balcony
- sensor.solcast_pv_forecast_peak_forecast_tomorrow | Solcast PV Forecast Peak Forecast Tomorrow | 482 W | area: Balcony
- sensor.solcast_pv_forecast_peak_time_today | Solcast PV Forecast Peak Time Today | 2025-10-20T10:00:00+00:00 | area:
  Balcony
- sensor.solcast_pv_forecast_peak_time_tomorrow | Solcast PV Forecast Peak Time Tomorrow | 2025-10-21T11:00:00+00:00 |
  area: Balcony
- sensor.solcast_pv_forecast_power_in_1_hour | Solcast PV Forecast Power in 1 Hour | 529 W | area: Balcony
- sensor.solcast_pv_forecast_power_in_30_minutes | Solcast PV Forecast Power in 30 Minutes | 624 W | area: Balcony
- sensor.solcast_pv_forecast_power_now | Solcast PV Forecast Power Now | 668 W | area: Balcony
- sensor.stades_ipad_activity | Stade’s iPad Activity | Stationary
- sensor.stades_ipad_app_version | Stade’s iPad App Version | 2025.10.0
- sensor.stades_ipad_audio_output | Stade’s iPad Audio Output | Built-in Speaker
- sensor.stades_ipad_battery_level | Stade’s iPad Battery Level | 95 %
- sensor.stades_ipad_battery_state | Stade’s iPad Battery State | Not Charging
- sensor.stades_ipad_bssid | Stade’s iPad BSSID | Not Connected
- sensor.stades_ipad_connection_type | Stade’s iPad Connection Type | Wi-Fi
- sensor.stades_ipad_geocoded_location | Stade’s iPad Geocoded Location | Schwiebusser Straße 45
  10965 Berlin
  Germany
- sensor.stades_ipad_last_update_trigger | Stade’s iPad Last Update Trigger | Siri
- sensor.stades_ipad_location_permission | Stade’s iPad Location permission | Authorized when in use
- sensor.stades_ipad_sim_1 | Stade’s iPad SIM 1 | --
- sensor.stades_ipad_ssid | Stade’s iPad SSID | Not Connected
- sensor.stades_ipad_storage | Stade’s iPad Storage | 42.02 % available
- sensor.stt | Home Assistant Speech-to-text | 0
- sensor.sun_next_dawn | Sun Next dawn | 2025-10-21T05:07:29+00:00
- sensor.sun_next_dusk | Sun Next dusk | 2025-10-20T16:35:37+00:00
- sensor.sun_next_midnight | Sun Next midnight | 2025-10-20T22:50:59+00:00
- sensor.sun_next_noon | Sun Next noon | 2025-10-21T10:51:03+00:00
- sensor.sun_next_rising | Sun Next rising | 2025-10-21T05:43:06+00:00
- sensor.sun_next_setting | Sun Next setting | 2025-10-20T16:00:09+00:00
- sensor.suns | Home Assistant Suns | 1
- sensor.switches | Home Assistant Switches | 103
- sensor.system_monitor_disk_free | System Monitor Disk free / | 217.7 GiB | area: Office
- sensor.system_monitor_disk_usage | System Monitor Disk usage / | 3.0 % | area: Office
- sensor.system_monitor_load_15m | System Monitor Load (15 min) | 0.11 | area: Office
- sensor.system_monitor_load_1m | System Monitor Load (1 min) | 0.13 | area: Office
- sensor.system_monitor_load_5m | System Monitor Load (5 min) | 0.16 | area: Office
- sensor.system_monitor_memory_free | System Monitor Memory free | 2860.9 MiB | area: Office
- sensor.system_monitor_memory_usage | System Monitor Memory usage | 28.3 % | area: Office
- sensor.system_monitor_memory_use | System Monitor Memory use | 1127.3 MiB | area: Office
- sensor.system_monitor_processor_temperature | System Monitor Processor temperature | 60.6 °C | area: Office
- sensor.system_monitor_processor_use | System Monitor Processor use | 2 % | area: Office
- sensor.system_monitor_swap_free | System Monitor Swap free | 1257.9 MiB | area: Office
- sensor.system_monitor_swap_usage | System Monitor Swap usage | 4.4 % | area: Office
- sensor.system_monitor_swap_use | System Monitor Swap use | 58.6 MiB | area: Office
- sensor.temperature_humidity_sensor_bc03_battery | Temperature/Humidity Sensor BC03 Battery | 49 % | area: Bathroom (
  En-Suite)
- sensor.temperature_humidity_sensor_bc03_humidity | Temperature/Humidity Sensor BC03 Humidity | 50.6 % | area:
  Bathroom (En-Suite)
- sensor.temperature_humidity_sensor_bc03_temperature | Temperature/Humidity Sensor BC03 Temperature | 23.3 °C | area:
  Bathroom (En-Suite)
- sensor.temperature_humidity_sensor_bc03_voltage | Temperature/Humidity Sensor BC03 Voltage | 2.641 V | area:
  Bathroom (En-Suite)
- sensor.temperature_humidity_sensor_d8b1_battery | Temperature/Humidity Sensor D8B1 Battery | 43 % | area: Bathroom
- sensor.temperature_humidity_sensor_d8b1_humidity | Temperature/Humidity Sensor D8B1 Humidity | 47.6 % | area: Bathroom
- sensor.temperature_humidity_sensor_d8b1_temperature | Temperature/Humidity Sensor D8B1 Temperature | 23.9 °C | area:
  Bathroom
- sensor.temperature_humidity_sensor_d8b1_voltage | Temperature/Humidity Sensor D8B1 Voltage | 2.587 V | area: Bathroom
- sensor.texts | Home Assistant Texts | 0
- sensor.times | Home Assistant Times | 2
- sensor.tts | Home Assistant Text-to-speech | 1
- sensor.update | Home Assistant Update | 26
- sensor.vacuum_filter_time_left_h | Vacuum Filter Time Left Hours | 20.6 h
- sensor.vacuum_last_duration_h | Vacuum Last Duration (h) | 1.5 h
- sensor.vacuum_main_brush_time_left_h | Vacuum Main Brush Time Left Hours | 170.6 h
- sensor.vacuum_mop_drying_time_left_h | Vacuum Mop Drying Time Left Hours | 0.0 h
- sensor.vacuum_sensor_time_left_h | Vacuum Sensor Time Left Hours | 24.6 h
- sensor.vacuum_side_brush_time_left_h | Vacuum Side Brush Time Left Hours | 70.6 h
- sensor.vacuum_total_cleaning_time_h | Vacuum Total Cleaning Time Hours | 129.4 h
- sensor.vacuums | Home Assistant Vacuums | 1
- sensor.water_heaters | Home Assistant Water heaters | 0
- sensor.weather | Home Assistant Weather | 2
- sensor.zones | Home Assistant Zones | 1

## sun (1)

- sun.sun | Sun | above_horizon

## switch (103)

- switch.35ad9eac_4306_4302_90e3_9930ecaa7be6_internet_access | 5421fd6e-7306-4d48-8394-6c0b0d6c1870 Internet Access |
  unavailable
- switch.appletv4k_internet_access | appletv4k Internet Access | on | area: Living Room
- switch.be1lf209_internet_access | BE1LF209 Internet Access | unavailable
- switch.brothermfc_l2710dw_internet_access | brothermfc-l2710dw Internet Access | on | area: Office
- switch.cloud_alexa | Home Assistant Cloud Alexa | unavailable
- switch.cloud_alexa_report_state | Home Assistant Cloud Alexa state reporting | unavailable
- switch.cloud_google | Home Assistant Cloud Google Assistant | unavailable
- switch.cloud_google_report_state | Home Assistant Cloud Google Assistant state reporting | unavailable
- switch.cloud_remote | Home Assistant Cloud Remote | unavailable
- switch.diskstationds918_internet_access | diskstationds918 Internet Access | on | area: Office
- switch.e3e81dda_ae46_46b9_b050_66e5bce85f7d_internet_access | e3e81dda-ae46-46b9-b050-66e5bce85f7d Internet Access |
  unavailable
- switch.echodotkids_internet_access | echodotkids-hans Internet Access | on | area: Kids Rooms
- switch.fritz_box_7590_ax_call_deflection_0 | FRITZ!Box 7590 AX Call deflection 0 | on | area: Office
- switch.fritz_box_7590_ax_call_deflection_1 | FRITZ!Box 7590 AX Call deflection 1 | on | area: Office
- switch.fritz_box_7590_ax_port_forward_http_server | FRITZ!Box 7590 AX Port forward HTTP-Server | unavailable | area:
  Office
- switch.fritz_box_7590_ax_port_forward_ssh | FRITZ!Box 7590 AX Port forward SSH | unavailable | area: Office
- switch.fritz_box_7590_ax_wi_fi_fritz_box_7590_if_2_4ghz | FRITZ!Box 7590 AX Wi-Fi FRITZ!Box 7590 IF (2.4Ghz) | on |
  area: Office
- switch.fritz_box_7590_ax_wi_fi_fritz_box_7590_if_5ghz | FRITZ!Box 7590 AX Wi-Fi FRITZ!Box 7590 IF (5Ghz) | on | area:
  Office
- switch.fritz_box_7590_ax_wi_fi_fritz_box_gastzugang | FRITZ!Box 7590 AX Wi-Fi FRITZ!Box Gastzugang | on | area: Office
- switch.fritz_repeater_internet_access | fritz.repeater Internet Access | unavailable
- switch.garminfenix7x_internet_access | garminfenix7x Internet Access | on
- switch.googlepixel6a_internet_access | googlepixel6a Internet Access | unavailable
- switch.homeassistant_internet_access | 2CCF678E8CB3 Internet Access | on
- switch.homepod_internet_access | homepod1-livingroom Internet Access | on
- switch.homepodmini1_office_internet_access | homepodmini1-office Internet Access | on
- switch.homepodmini2_office_internet_access | homepodmini2-office Internet Access | on
- switch.homepodmini_kitchen_internet_access | homepodmini-kitchen Internet Access | on | area: Kitchen
- switch.hoymileshms_800w_2t_internet_access | hoymileshms-800w-2t Internet Access | on | area: Balcony
- switch.ipad_internet_access | iPad Internet Access | unavailable
- switch.ipadpro_internet_access | ipadpro Internet Access | on
- switch.iphone12pro_internet_access | iphone12pro Internet Access | on
- switch.iphone13_work_internet_access | iphone13-work Internet Access | unavailable
- switch.iphone_internet_access | iPhone Internet Access | unavailable
- switch.iphone_internet_access_2 | iPhone Internet Access | unavailable
- switch.iphone_internet_access_3 | iPhone Internet Access | unavailable
- switch.iphone_internet_access_4 | iPhone Internet Access | unavailable
- switch.iphone_internet_access_5 | iPhone-XFL7DN71P2 Internet Access | unavailable
- switch.iphone_internet_access_6 | iPhone Internet Access | on
- switch.kindlepaperwhite_internet_access | kindlepaperwhite Internet Access | on
- switch.lenovo_internet_access | Lenovo Internet Access | unavailable
- switch.living_room_3_internet_access | Living-Room-3 Internet Access | on
- switch.living_room_internet_access | Living-Room Internet Access | unavailable
- switch.mac_internet_access | Mac Internet Access | unavailable
- switch.mac_internet_access_2 | Mac Internet Access | on
- switch.macbookair_dennis_internet_access | macbookair-dennis Internet Access | unavailable
- switch.macbookair_internet_access | MacBookAir Internet Access | on
- switch.macbookair_kristin_internet_access | macbookair-kristin Internet Access | unavailable
- switch.macbookpro14_work_internet_access | macbookpro14-work Internet Access | unavailable | area: Office
- switch.macbookpro14_work_internet_access_2 | macbookpro14-work Internet Access | on | area: Office
- switch.macbookpro16_internet_access | macbookpro16 Internet Access | unavailable | area: Office
- switch.macbookpro_internet_access | MacBookPro Internet Access | on
- switch.meross_smart_plug_internet_access | meross-smart-plug-refrigerator Internet Access | on | area: Kitchen
- switch.meross_smart_plug_internet_access_2 | meross-smart-plug-dishwasher Internet Access | on | area: Kitchen
- switch.meross_smart_plug_internet_access_3 | Meross-Smart-Plug Internet Access | on | area: Living Room
- switch.meross_smart_plug_laundry_internet_access | meross-smart-plug-laundry Internet Access | on | area: Office
- switch.meross_smart_plug_living_room_config_overtemp_enable | Meross-Smart-Plug (Living Room) Config overtemp enable |
  on | area: Living Room
- switch.meross_smart_plug_living_room_outlet | Meross-Smart-Plug (Living Room) Outlet | on | area: Living Room
- switch.meross_smart_plug_livingroom_internet_access | meross-smart-plug-livingroom Internet Access | on | area: Living
  Room
- switch.meross_smart_plug_office_internet_access | meross-smart-plug-office Internet Access | on | area: Bathroom
- switch.mileddesklamp1s_internet_access | mileddesklamp1s Internet Access | on | area: Office
- switch.netatmosmarthomeweatherstation_internet_access | netatmosmarthomeweatherstation Internet Access | on
- switch.none_2_internet_access | echodotkids-vicky Internet Access | on
- switch.pc_00_24_e4_4b_f9_10_internet_access | PC-00-24-E4-4B-F9-10 Internet Access | unavailable
- switch.pc_18e6_c2f3_c544_2770_internet_access | homepod2-livingroom Internet Access | on
- switch.pc_192_168_178_125_internet_access | PC-A4-7E-FA-07-2B-82 Internet Access | on
- switch.pc_192_168_178_74_internet_access | iPhone Internet Access | unavailable
- switch.pc_192_168_178_78_internet_access | PC-192-168-178-78 Internet Access | unavailable
- switch.pc_192_168_178_79_internet_access | PC-192-168-178-79 Internet Access | unavailable
- switch.pc_192_168_178_93_internet_access | PC-192-168-178-93 Internet Access | unavailable
- switch.pc_62_ab_eb_2e_bd_76_internet_access | iPhone Internet Access | on
- switch.pc_7a_94_d2_d1_01_80_internet_access | PC-7A-94-D2-D1-01-80 Internet Access | unavailable
- switch.pc_7a_9f_4b_0f_87_84_internet_access | Watch Internet Access | on
- switch.pc_b6_89_c2_97_56_30_internet_access | iPad Internet Access | unavailable
- switch.raspberrypi4_internet_access | raspberrypi4 Internet Access | unavailable
- switch.raspberrypi_internet_access | homeassistant Internet Access | unavailable
- switch.rdde01rn_internet_access | RDDE01RN Internet Access | unavailable
- switch.roborock_qrevo_pro_do_not_disturb | Roborock Qrevo Pro Do not disturb | off | area: Office
- switch.roborock_qrevo_pro_dock_child_lock | Roborock Qrevo Pro Dock Child lock | off | area: Office
- switch.roborock_vacuum_a101_internet_access | roborockqrevopro Internet Access | on | area: Office
- switch.roborockq7max_internet_access | roborockq7max Internet Access | unavailable | area: Office
- switch.samsunggalaxys7_internet_access | samsunggalaxys7 Internet Access | on
- switch.shellyplugsg3_28372f2f1e04 | Shelly Plug S (E-Bike) | on | area: Office
- switch.shellyplugsg3_28372f2f1e04_internet_access | shellyplugs-ebike Internet Access | on | area: Office
- switch.shellyplusplugs_d4d4da363900 | Shelly Plug S (Office) | on | area: Office
- switch.shellyplusplugs_d4d4da363900_internet_access | shellyplugs-office Internet Access | on | area: Office
- switch.shellypmminigen3_balcony_internet_access | shellypmminigen3-balcony Internet Access | on | area: Balcony
- switch.shellypro3em_08f9e0e88160_internet_access | shellypro3em Internet Access | on
- switch.shellypro3em_08f9e0e88160_internet_access_2 | Shelly Pro 3EM Internet Access | unavailable | area: Office
- switch.smart_plug_19011801871415251h0334298f1a2070_outlet | Washing Machine Outlet | on | area: Bathroom
- switch.smart_plug_1908212877531725185548e1e90233ca_outlet | Meross-Smart-Plug (Dishwasher) Outlet | on | area: Kitchen
- switch.smart_plug_1908213017294825185548e1e9024169_outlet | Meross-Smart-Plug (Refrigerator) Outlet | on | area:
  Kitchen
- switch.smart_plug_1908215645566225185548e1e9023170_outlet | Roborock Qrevo Pro Outlet | on | area: Office
- switch.smart_plug_1908218495823925185548e1e9023052_outlet | Living room lamp Outlet | off | area: Living Room
- switch.toniebox_internet_access | Toniebox Internet Access | on | area: Kids Rooms
- switch.watch_internet_access | Watch Internet Access | unavailable
- switch.watch_internet_access_2 | Watch Internet Access | unavailable
- switch.withingsbodycardio_internet_access | withingsbodycardio Internet Access | on | area: Bedroom
- switch.wsc513101001578_internet_access | WSC513101001578 Internet Access | unavailable
- switch.yeelightceilinglight_diningroom_internet_access | yeelightceilinglight-diningroom Internet Access | on
- switch.yeelightceilinglight_hans_internet_access | yeelightceilinglight-hans Internet Access | on
- switch.yeelightceilinglight_livingroom_internet_access | yeelightceilinglight-livingroom Internet Access | on
- switch.yeelightceilinglight_office_internet_access | yeelightceilinglight-office Internet Access | on
- switch.yeelink_light_ceiling11_miiof2_internet_access | yeelightceilinglight-bedroom Internet Access | on

## tag (1)

- tag.efffef5f_db7b_4ecc_800f_c41896c17f5f | Tag efffef5f-db7b-4ecc-800f-c41896c17f5f | 2025-10-14T15:49:57.976+00:00

## time (2)

- time.roborock_qrevo_pro_do_not_disturb_begin | Roborock Qrevo Pro Do not disturb begin | 22:00:00 | area: Office
- time.roborock_qrevo_pro_do_not_disturb_end | Roborock Qrevo Pro Do not disturb end | 07:00:00 | area: Office

## todo (1)

- todo.shopping_list | Shopping List | 0

## tts (1)

- tts.google_en_com | Google Translate en com | unknown

## update (26)

- update.alexa_media_player_update | Alexa Media Player update | off
- update.apexcharts_card_update | apexcharts-card update | off
- update.auto_backup_update | Auto Backup update | off
- update.battery_state_card_entity_row_update | Battery State Card / Entity Row update | off
- update.button_card_update | button-card update | off
- update.diskstation_dsm_update | DiskStation DSM update | off | area: Office
- update.file_editor_update | File editor Update | off
- update.fritz_box_7590_ax_fritz_os | FRITZ!Box 7590 AX FRITZ!OS | off | area: Office
- update.fritz_repeater_2400_fritz_os | FRITZ!Repeater 2400 FRITZ!OS | unavailable | area: Living Room
- update.get_hacs_update | Get HACS Update | off
- update.hacs_update | HACS update | off
- update.home_assistant_core_update | Home Assistant Core Update | off
- update.home_assistant_operating_system_update | Home Assistant Operating System Update | off
- update.home_assistant_supervisor_update | Home Assistant Supervisor Update | off
- update.layout_card_update | layout-card update | off
- update.matter_server_update | Matter Server Update | off
- update.meross_lan_update | Meross LAN update | off
- update.mini_graph_card_update | mini-graph-card update | off
- update.mushroom_update | Mushroom update | off
- update.shellyplugsg3_28372f2f1e04_firmware | Shelly Plug S (E-Bike) Firmware | off | area: Office
- update.shellyplusplugs_d4d4da363900_firmware | Shelly Plug S (Office) Firmware | off | area: Office
- update.shellypmminig3_dcda0ce9c28c_firmware_update | Shelly PM Mini Gen3 (Balcony) firmware update | off | area:
  Balcony
- update.shellypro3em_08f9e0e88160_firmware_update | Shelly Pro 3EM firmware update | off | area: Office
- update.solcast_pv_forecast_update | Solcast PV Forecast update | off
- update.spook_your_homie_update | Spook 👻 Your homie update | off
- update.weather_card_update | Weather Card update | off

## vacuum (1)

- vacuum.roborock_qrevo_pro | Roborock Qrevo Pro | docked | area: Office

## weather (2)

- weather.forecast_home | Forecast Home | partlycloudy
- weather.openweathermap | OpenWeatherMap | sunny | area: Balcony

## zone (1)

- zone.home | Home | 1
