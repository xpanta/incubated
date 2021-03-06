# GovCT1
type: "object"
description : >
## Description
General model for any prime mover with a PID governor, used primarily for combustion turbine and combined cycle units. This model can be used to represent a variety of prime movers controlled by PID governors.  It is suitable, for example, for representation of     Additional information on this model is available in the 2012 IEEE report, , section 3.1.2.3 page 3-4 (GGOV1).

## Data Model
  - properties:
    - mwbase:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Base for power values (MWbase) (> 0).  Unit = MW. Default: 0.0
    - r:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Permanent droop (R).  Typical Value = 0.04. Default: 0.0
    - rselect:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Feedback signal for droop (Rselect).  Typical Value = electricalPower. Default: None
    - tpelec:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Electrical power transducer time constant (Tpelec) (>0).  Typical Value = 1. Default: 0
    - maxerr:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Maximum value for speed error signal (maxerr).  Typical Value = 0.05. Default: 0.0
    - minerr:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Minimum value for speed error signal (minerr).  Typical Value = -0.05. Default: 0.0
    - kpgov:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Governor proportional gain (Kpgov).  Typical Value = 10. Default: 0.0
    - kigov:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Governor integral gain (Kigov).  Typical Value = 2. Default: 0.0
    - kdgov:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Governor derivative gain (Kdgov).  Typical Value = 0. Default: 0.0
    - tdgov:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Governor derivative controller time constant (Tdgov).  Typical Value = 1. Default: 0
    - vmax:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Maximum valve position limit (Vmax).  Typical Value = 1. Default: 0.0
    - vmin:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Minimum valve position limit (Vmin).  Typical Value = 0.15. Default: 0.0
    - tact:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Actuator time constant (Tact).  Typical Value = 0.5. Default: 0
    - kturb:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Turbine gain (Kturb) (>0).  Typical Value = 1.5. Default: 0.0
    - wfnl:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : No load fuel flow (Wfnl).  Typical Value = 0.2. Default: 0.0
    - tb:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Turbine lag time constant (Tb) (>0).  Typical Value = 0.5. Default: 0
    - tc:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Turbine lead time constant (Tc).  Typical Value = 0. Default: 0
    - wfspd:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Switch for fuel source characteristic to recognize that fuel flow, for a given fuel valve stroke, can be proportional to engine speed (Wfspd). true = fuel flow proportional to speed (for some gas turbines and diesel engines with positive displacement fuel injectors) false = fuel control system keeps fuel flow independent of engine speed. Typical Value = true. Default: False
    - teng:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Transport time delay for diesel engine used in representing diesel engines where there is a small but measurable transport delay between a change in fuel flow setting and the development of torque (Teng).  Teng should be zero in all but special cases where this transport delay is of particular concern.  Typical Value = 0. Default: 0
    - tfload:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Load Limiter time constant (Tfload) (>0).  Typical Value = 3. Default: 0
    - kpload:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Load limiter proportional gain for PI controller (Kpload).  Typical Value = 2. Default: 0.0
    - kiload:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Load limiter integral gain for PI controller (Kiload).  Typical Value = 0.67. Default: 0.0
    - ldref:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Load limiter reference value (Ldref).  Typical Value = 1. Default: 0.0
    - dm:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Speed sensitivity coefficient (Dm).  Dm can represent either the variation of the engine power with the shaft speed or the variation of maximum power capability with shaft speed.  If it is positive it describes the falling slope of the engine speed verses power characteristic as speed increases. A slightly falling characteristic is typical for reciprocating engines and some aero-derivative turbines.  If it is negative the engine power is assumed to be unaffected by the shaft speed, but the maximum permissible fuel flow is taken to fall with falling shaft speed. This is characteristic of single-shaft industrial turbines due to exhaust temperature limits.  Typical Value = 0. Default: 0.0
    - ropen:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Maximum valve opening rate (Ropen).  Unit = PU/sec.  Typical Value = 0.10. Default: 0.0
    - rclose:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Minimum valve closing rate (Rclose).  Unit = PU/sec.  Typical Value = -0.1. Default: 0.0
    - kimw:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Power controller (reset) gain (Kimw).  The default value of 0.01 corresponds to a reset time of 100 seconds.  A value of 0.001 corresponds to a relatively slow acting load controller.  Typical Value = 0.01. Default: 0.0
    - aset:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Acceleration limiter setpoint (Aset).  Unit = PU/sec.  Typical Value = 0.01. Default: 0.0
    - ka:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Acceleration limiter gain (Ka).  Typical Value = 10. Default: 0.0
    - ta:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Acceleration limiter time constant (Ta) (>0).  Typical Value = 0.1. Default: 0
    - db:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Speed governor dead band in per unit speed (db).  In the majority of applications, it is recommended that this value be set to zero.  Typical Value = 0. Default: 0.0
    - tsa:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Temperature detection lead time constant (Tsa).  Typical Value = 4. Default: 0
    - tsb:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Temperature detection lag time constant (Tsb).  Typical Value = 5. Default: 0
    - rup:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Maximum rate of load limit increase (Rup).  Typical Value = 99. Default: 0.0
    - rdown:
      - x-ngsi:
        - type: Property
        - model: https://schema.org/Number
      - type: "number"
      - description: : Maximum rate of load limit decrease (Rdown).  Typical Value = -99. Default: 0.0
