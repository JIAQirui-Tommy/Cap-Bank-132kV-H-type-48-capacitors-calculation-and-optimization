# 132kV H Type 48 Capacitor Bank Unbalanced Current Optimization

Static web tool for calculating and reducing unbalanced current in a 132kV H type capacitor bank.

Live app: https://jiaqirui-tommy.github.io/Cap-Bank-132kV-H-type-48-capacitors-calculation-and-optimization/

## Configuration

- 48 capacitors total
- Four H bridge arms: C1 Front Top, C2 Front Bottom, C3 Rear Top, C4 Rear Bottom
- Capacitors are numbered 1-48: C1 is 1-12, C2 is 13-24, C3 is 25-36, and C4 is 37-48
- Each arm has 12 capacitors
- Each parallel group has 2 capacitors
- Each arm has 6 parallel groups in series
- Relay / CT branch is calculated using the approximate short-circuit model
- CT ratio is entered as `primary:1`; secondary unbalanced current is primary current divided by the CT primary ratio
- Visual guide maps C1/C2 to C1 Front Top / C2 Front Bottom and C3/C4 to C3 Rear Top / C4 Rear Bottom

## Use

Open `index.html` in a browser, enter the measured capacitance values, choose the number of swap pairs, and run `Optimize swaps`.
Use `Download Template` to get `capbank_48_template.xlsx`, fill the `Capacitance uF` column, then load it back into the current phase.
