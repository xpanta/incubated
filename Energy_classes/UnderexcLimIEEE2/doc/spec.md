# UnderexcLimIEEE2
type: "object"
description : >
## Description
The class represents the Type UEL2 which has either a straight-line or multi-segment characteristic when plotted in terms of machine reactive power output vs. real power output.  Reference: IEEE UEL2 421.5-2005 Section 10.2.  (Limit characteristic lookup table shown in Figure 10.4 (p 32) of the standard).

## Data Model
  - properties:
    - tuv:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Voltage filter time constant (T).  Typical Value = 5. Default: 0
    - tup:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Real power filter time constant (T).  Typical Value = 5. Default: 0
    - tuq:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Reactive power filter time constant (T).  Typical Value = 0. Default: 0
    - kui:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : UEL integral gain (K).  Typical Value = 0.5. Default: 0.0
    - kul:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : UEL proportional gain (K).  Typical Value = 0.8. Default: 0.0
    - vuimax:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : UEL integrator output maximum limit (V).  Typical Value = 0.25. Default: 0.0
    - vuimin:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : UEL integrator output minimum limit (V).  Typical Value = 0. Default: 0.0
    - kuf:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : UEL excitation system stabilizer gain (K).  Typical Value = 0. Default: 0.0
    - kfb:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Gain associated with optional integrator feedback input signal to UEL (K).  Typical Value = 0. Default: 0.0
    - tul:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Time constant associated with optional integrator feedback input signal to UEL (T).  Typical Value = 0. Default: 0
    - tu1:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : UEL lead time constant (T).  Typical Value = 0. Default: 0
    - tu2:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : UEL lag time constant (T).  Typical Value = 0. Default: 0
    - tu3:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : UEL lead time constant (T).  Typical Value = 0. Default: 0
    - tu4:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : UEL lag time constant (T).  Typical Value = 0. Default: 0
    - vulmax:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : UEL output maximum limit (V).  Typical Value = 0.25. Default: 0.0
    - vulmin:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : UEL output minimum limit (V).  Typical Value = 0. Default: 0.0
    - p0:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Real power values for endpoints (P).  Typical Value = 0. Default: 0.0
    - q0:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Reactive power values for endpoints (Q).  Typical Value = -0.31. Default: 0.0
    - p1:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Real power values for endpoints (P).  Typical Value = 0.3. Default: 0.0
    - q1:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Reactive power values for endpoints (Q).  Typical Value = -0.31. Default: 0.0
    - p2:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Real power values for endpoints (P).  Typical Value = 0.6. Default: 0.0
    - q2:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Reactive power values for endpoints (Q).  Typical Value = -0.28. Default: 0.0
    - p3:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Real power values for endpoints (P).  Typical Value = 0.9. Default: 0.0
    - q3:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Reactive power values for endpoints (Q).  Typical Value = -0.21. Default: 0.0
    - p4:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Real power values for endpoints (P).  Typical Value = 1.02. Default: 0.0
    - q4:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Reactive power values for endpoints (Q).  Typical Value = 0. Default: 0.0
    - p5:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Real power values for endpoints (P). Default: 0.0
    - q5:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Reactive power values for endpoints (Q). Default: 0.0
    - p6:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Real power values for endpoints (P). Default: 0.0
    - q6:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Reactive power values for endpoints (Q). Default: 0.0
    - p7:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Real power values for endpoints (P). Default: 0.0
    - q7:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Reactive power values for endpoints (Q). Default: 0.0
    - p8:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Real power values for endpoints (P). Default: 0.0
    - q8:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Reactive power values for endpoints (Q). Default: 0.0
    - p9:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Real power values for endpoints (P). Default: 0.0
    - q9:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Reactive power values for endpoints (Q). Default: 0.0
    - p10:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Real power values for endpoints (P). Default: 0.0
    - q10:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Reactive power values for endpoints (Q). Default: 0.0
    - k1:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : UEL terminal voltage exponent applied to real power input to UEL limit look-up table (k1).  Typical Value = 2. Default: 0.0
    - k2:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : UEL terminal voltage exponent applied to reactive power output from UEL limit look-up table (k2).  Typical Value = 2. Default: 0.0
