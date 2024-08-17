## Optimization of Aspect Ratio for Cooling Channels in Rocket Engines

**Project description:** This project focuses on finding the optimal aspect ratio (AR), and optimal mass flow rate for cooling channels in the RL10 engine, with the goal of minimizing power loss while maintaining effective cooling. The study involves a parametric analysis, where different aspect ratios, and flow rates are tested to observe their effects on pressure drop, and power loss in the cooling system.

### 1. Objective and Methodology

The primary objective of this study is to identify the optimal AR that minimizes the power required by the pumps while ensuring the coolant remains subsonic and the wall temperature stays below 970K. The design consists in:
- **Design:** Fixed channel height with the width as twice the rib thickness.

### 2. Key Equations and Concepts
- **Aspect Ratio (AR):** Ratio of channel height to width.
- **Heat Transfer Coefficient:** Derived using the Dittus-Boelter correlation for the Nusselt number.
- **Wetted Perimeter & Hydraulic Diameter:** Influences pressure drop and heat transfer efficiency.

### 3. Requirements
- Wall temperature below 1200K (maximum allowed for Copper-Nickel Alloy)
- Cooling channels outlet pressure = 5.6 MPa
- Coolant remains subsonic in the channels

### 4. Results and Analysis

![Graphical Results](images/plot7.jpg){:width="800px" height="300px"}

The results indicated that there is a minimum pump power required at AR=6


### 5. Discussion

- This study reveals a trade-off between enhancing cooling capabilities and managing pressure losses as AR increases.
- Using a mass flow rate of 3.7 kg/s instead of the initial choice of 4 kg/s, with an aspect ratio of 6, **will save 6% on pump power required**, while still meeting the requirements of wall cooling and channles outlet pressure.

```javascript
// Example of iterative method used in the study (bisection method for pressure drop)
function [P_out] = get_CJ_inlet_pressure(minAR, maxAR)
  while (P_lower - P_upper)/P_upper > tolerance)
    P_mid = (P_lower + P_upper) / 2;
    P_out_mid = cooling_function(P_mid);
    err_mid = P_out - P_out_mid;
    if err_low * err_mid > 0
      P_lower = P_mid;
      err_lower = err_mid;
    else  
      P_upper = P_mid;
    end
    if abs(err_mid) < tol
      run = 0;
    end
  end
end
```
### 6. Conclusion and Future Work
The optimal AR for minimizing power loss while maintaining effective cooling is AR=10 for Design 1. Future work could explore additional variables or different cooling channel geometries to further optimize performance.

[Project PDF](/pdf/Marco_Nanni_Presentation_Portfolio.pdf)
