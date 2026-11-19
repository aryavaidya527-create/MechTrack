# MechTrack v1.0.0 — Phase 1 release notes

## Included in this release

- Production batch entry, edit, delete, yield, and output-rate calculation
- Maintenance task entry, edit, delete, status changes, and optional cost
- Motor shaft torque and power calculations
- Editable machine profile
- CSV export for production and maintenance records
- Local browser storage, CSV backup guidance, and responsive layout

## Release checks to complete before public announcement

- Add a production batch using test data and confirm the dashboard totals update.
- Edit and delete that batch; confirm the dashboard updates again.
- Add a maintenance task, mark it complete, then reopen it.
- Export both CSV files and open them in a spreadsheet to confirm the values.
- Test torque with 1 kW at 1000 RPM (expected ideal estimate: 9.55 N·m).
- Refresh the page and confirm records remain in the same browser.
- Use a generic machine profile. Share internship or employer-owned specifications only when you have permission.

## Known limitations

Data is local to one browser/device. This release has no backend, accounts, multi-device synchronization, sensor connectivity, or machine control. The calculator provides ideal shaft estimates only.
