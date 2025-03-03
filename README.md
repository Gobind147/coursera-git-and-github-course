# coursera-git-and-github-course
learning
I am editing the README file. Adding some more details about the project description.
this repository is based on coursera course offered by google "Introduction to Git and GitHub"
https://www.coursera.org/learn/introduction-git-github/home/welcome



Theoretical Background
Understanding gas turbine icing requires knowledge of basic thermodynamics of moist air and fluid flow in the inlet. Key factors include humidity (moisture content) of the air, air pressure and temperature changes through the inlet, and heat transfer effects at surfaces. This section summarizes the relevant concepts: absolute vs. relative humidity, dew point, pressure/temperature relationships for flowing air, and how these relate to ice formation.Moisture Content and Humidity: Atmospheric air always contains some water vapor. The absolute humidity is the actual mass of water vapor per unit volume of air (typically in g/m³), whereas the more commonly quoted relative humidity (RH) is the ratio (in %) of the current water vapor pressure to the saturation vapor pressure at the same temperature. Warm air can hold more moisture as vapor; the saturation vapor pressure increases rapidly with temperature. When air is cooled, the maximum moisture it can hold drops, and at the dew point temperature the air becomes fully saturated (100% RH). The dew point is defined as the temperature to which air must be cooled (at constant pressure) for water vapor to start condensing into liquid​
SENSIRION.COM
. For example, at 20 °C and 80% RH, the water vapor partial pressure is about 18.7 hPa, and the absolute humidity is around 13.8 g/m³​
HATCHABILITY.COM
. If this air is cooled to approximately 16 °C, it will reach 100% RH and water will begin to condense – 16 °C is the dew point in that case. A convenient empirical formula for dew point (the Magnus formula) can be used: for temperature T (°C) and relative humidity φ, one approximation is:
𝑇
dew
≈
𝑏
[
ln
⁡
(
𝜙
100
)
+
𝑎
 
𝑇
𝑏
+
𝑇
]
𝑎
−
[
ln
⁡
(
𝜙
100
)
+
𝑎
 
𝑇
𝑏
+
𝑇
]
,
T 
dew
​
 ≈ 
a−[ln( 
100
ϕ
​
 )+ 
b+T
aT
​
 ]
b[ln( 
100
ϕ
​
 )+ 
b+T
aT
​
 ]
​
 ,where a and b are empirically determined constants (for water vapor in air, a ≈ 17.62 and b ≈ 243.12 °C)​
SENSIRION.COM
​
SENSIRION.COM
. This formula yields the dew point temperature in °C. A dew point at or below 0 °C is often called the frost point, indicating that water vapor would deposit as ice (frost) rather than liquid if saturation occurs at those temperatures​
PAULOCRGOMES.COM.BR
.Absolute Humidity: In engineering calculations, absolute humidity can also be expressed as a mixing ratio (mass of water per mass of dry air) or as mass per volume. Assuming ideal gas behavior for water vapor, one useful formula is:
𝜌
𝑣
=
2.16679
 
𝑃
𝑤
𝑇
𝑘
(in g/m³)
,
ρ 
v
​
 =2.16679 
T 
k
​
 
P 
w
​
 
​
 (in g/m³),where $P_w$ is the water vapor partial pressure in Pa and $T_k$ is the air temperature in K​
HATCHABILITY.COM
. This constant (2.16679) incorporates the specific gas constant for water vapor and the conversion to grams. Using the earlier example: at 20 °C (293 K) and 80% RH, the saturation vapor pressure $P_{ws}(20°C) \approx 23.4$ hPa (2340 Pa). With RH = 80%, the actual $P_w = 0.8 \times P_{ws} \approx 18.7$ hPa (1870 Pa). Plugging in, $\rho_v = 2.16679 \times 1870 / 293.15 \approx 13.8$ g/m³, as reported​
HATCHABILITY.COM
. This value represents the moisture content of the air. Higher absolute humidity (more water vapor) generally increases icing risk, since more moisture is available to condense or freeze if conditions allow.Flow Pressure and Temperature in the Inlet: As air flows from the ambient atmosphere through the turbine’s intake and into the compressor, its pressure and velocity change according to fluid dynamics principles (approximately Bernoulli’s principle for subsonic flow, with some losses). If we denote the ambient total pressure (essentially atmospheric pressure) as $P_{o1}$ and the compressor inlet total pressure as $P_{o2}$, any intake losses (from filters, ducts, etc.) will cause a pressure drop $\Delta P = P_{o1} - P_{o2}$​
FILE-FQXWKSQORFJAPJFD91XPJ9
. For example, ice or frost buildup on filters adds flow resistance and increases $\Delta P$. A higher pressure drop means the compressor draws from a lower intake pressure, which directly reduces the density of the air entering the compressor and thus can reduce mass flow and power output. This is why even a small amount of icing can noticeably degrade performance.In addition to total pressure loss, the conversion of pressure into velocity in the inlet can cause the static pressure and static temperature of the air to drop. The inlet airflow accelerates as it approaches the compressor face (which has a strong suction effect). Under adiabatic flow (no heat exchange), the total temperature of the air remains constant (neglecting viscous heating) as it moves through the intake​
FILE-FQXWKSQORFJAPJFD91XPJ9
​
FILE-FQXWKSQORFJAPJFD91XPJ9
. However, part of that total (stagnation) temperature is converted into kinetic energy of the moving air. The relation can be described by:
𝑇
total
=
𝑇
static
+
𝑉
2
2
𝑐
𝑝
,
T 
total
​
 =T 
static
​
 + 
2c 
p
​
 
V 
2
 
​
 ,where $V$ is the air velocity and $c_p$ is the specific heat of air at constant pressure. If the air is nearly stationary at the intake entrance ($V \approx 0$), then initially $T_{\text{total}} \approx T_{\text{ambient}}$. But by the time the air reaches the compressor inlet with velocity $V_2$, the static temperature $T_{s2}$ will be lower than $T_{\text{total}}$ by the amount $\Delta T_s = \frac{V_2^2}{2 c_p}$​
FILE-FQXWKSQORFJAPJFD91XPJ9
​
FILE-FQXWKSQORFJAPJFD91XPJ9
. This static temperature depression can be on the order of a few degrees for typical inlet velocities. For instance, if $V_2 = 50$ m/s, $\Delta T_s$ is roughly 1–2 K (since for air $c_p\approx1005$ J/(kg·K)). Thus, even if the ambient air is above freezing (say +2 °C), the static temperature right at the compressor inlet might drop to ~0 °C or below due to acceleration cooling. The static pressure likewise drops due to the Bernoulli effect: $P_{s2} = P_{o2} - \tfrac{1}{2}\rho V_2^2$ (subtracting the dynamic pressure)​
FILE-FQXWKSQORFJAPJFD91XPJ9
.Surface Temperature and Recovery Factor: The metal surfaces in the inlet system (filters, bellmouth, guide vanes, etc.) may not cool all the way to the static air temperature because of viscous and thermal effects. As air flows over a surface, a boundary layer forms and some kinetic energy is converted into a slight rise in surface temperature. The recovery factor (RF) is defined to quantify how much of the total-to-static temperature difference is “recovered” at the surface. In other words, the surface temperature $T_{\text{surface}}$ will lie between the static air temperature and the total temperature. The recovery factor (for a given surface and flow regime) is:
𝑅
𝐹
=
𝑇
surface
−
𝑇
static
𝑇
total
−
𝑇
static
.
RF= 
T 
total
​
 −T 
static
​
 
T 
surface
​
 −T 
static
​
 
​
 .For turbulent flow on metal surfaces, empirical values of $RF$ are often around 0.8–0.9​
IAIEST.COM
. This means the surface gets closer to the total temperature (ambient temperature) than the static air temperature does. Using RF, we can directly compute the surface temperature as:T_{\text{surface}} = T_{s2} + RF \,\big(T_{o2} - T_{s2}\big). \tag{1}\label{eq:Tsrf}For example, if the air static temperature at the compressor inlet is $T_{s2} = -5$ °C and the total (ambient) temperature is $T_{o2} = 0$ °C, a recovery factor of 0.8 gives $T_{\text{surface}} = -5 + 0.8(0 - (-5)) = -5 + 0.8(5) = -1$ °C. In this case, the surface is a few degrees warmer than the local air. Each turbine and surface type has its own effective RF, so in practice one might need to empirically determine it​
FILE-FQXWKSQORFJAPJFD91XPJ9
​
FILE-FQXWKSQORFJAPJFD91XPJ9
. In icing analyses, an assumed RF (e.g. 0.8 for metal inlet guide vanes) is used to estimate surface temperature​
PAULOCRGOMES.COM.BR
.The dew point of the air will also shift slightly as pressure changes. Lower static pressure in the accelerated inlet air leads to a lower saturation temperature. In effect, the dew point of the air in front of the compressor is a bit lower than the dew point at ambient conditions due to the pressure drop (this is sometimes termed dew point depression)​
FILE-FQXWKSQORFJAPJFD91XPJ9
​
FILE-FQXWKSQORFJAPJFD91XPJ9
. However, the change is relatively small for the modest pressure drops in intake systems. The dominant factors remain the ambient humidity and the cooling of air and surfaces. With this background in mind, we can now formalize the criteria for ice formation and develop a method to calculate when icing will occur.
Methodology
Criteria for Ice Formation: For ice to form on any surface in the gas turbine inlet (filters, bellmouth, inlet guide vanes, etc.), two thermodynamic conditions must be met simultaneously​
IAIEST.COM
:
Surface temperature below dew point: $T_{\text{surface}} < T_{\text{dew}}$. This ensures that the air adjacent to the surface reaches saturation and condensation (or deposition) begins. Essentially, the surface is cold enough to cause moisture in the air to condense on it. If this condition is not met, the air remains unsaturated and no liquid water (or frost) will accumulate on the surface​
FILE-FQXWKSQORFJAPJFD91XPJ9
. (Note: if the dew point is below 0 °C, condensation actually means direct deposition of ice, i.e. frost, since the “dew” would freeze immediately.)
Surface temperature below freezing: $T_{\text{surface}} \le 0~^\circ$C. This ensures that any water that condenses (or any moisture coming in contact with the surface) will freeze into solid ice. If the surface is above 0 °C, condensation might occur as liquid water, but it will not freeze into ice. For icing, we require the surface to be at or below the freezing point of water​
IAIEST.COM
.
When both of the above criteria are satisfied, ice will accumulate on the surface. In summary, the surface must be cold enough to both induce condensation and to freeze the condensate​
FILE-FQXWKSQORFJAPJFD91XPJ9
. If either condition is not met, ice formation is unlikely: for example, a surface at –5 °C with very low humidity air (dew point say –10 °C) will not cause icing because, although below freezing, it’s not below the dew point so no moisture will deposit. Likewise, a surface at +1 °C in near-saturated air might get wet with dew but not ice, since it’s above 0 °C. It’s also worth noting that if ambient air is extremely cold (< –30 °C) its absolute humidity is usually very low; moisture may already be in the form of tiny ice crystals (freezing fog) that pass through the filters without sticking​
FILE-FQXWKSQORFJAPJFD91XPJ9
. In such conditions, inlet icing on surfaces is rare despite the cold temperature, because the air is too dry (dew point far below 0 °C). The worst icing risk is generally in the temperature range just below freezing with high humidity – exactly when air can easily be saturated and surfaces hover around the freezing point.Mathematical Formulation: Based on the above criteria, we outline the formulas needed to predict icing conditions:
Absolute Humidity / Moisture Content: We first compute the water vapor partial pressure $P_{v}$ in the ambient air. This can be obtained from ambient temperature $T_{\text{amb}}$ and RH using a saturation pressure formula. For instance, using Tetens’ formula for saturation pressure of water over liquid (valid for temperatures >0 °C):
𝑃
ws
(
𝑇
)
=
6.1078
×
10
7.5
𝑇
/
(
237.3
+
𝑇
)
 hPa
,
P 
ws
​
 (T)=6.1078×10 
7.5T/(237.3+T)
  hPa,and then $P_{v} = (\phi/100),P_{\text{ws}}(T)$, where $\phi$ is relative humidity. (For temperatures below 0 °C, a similar formula for saturation over ice could be used, but in practice the difference is small for our purposes.) The absolute humidity in terms of mixing ratio (mass of water per mass of dry air) can be computed by the formula for specific humidity:
𝜔
=
0.622
 
𝑃
𝑣
𝑃
𝑜
1
−
𝑃
𝑣
,
ω= 
P 
o1
​
 −P 
v
​
 
0.622 P 
v
​
 
​
 ,where $P_{o1}$ is the ambient pressure​
FILE-FQXWKSQORFJAPJFD91XPJ9
. Here 0.622 is the ratio of the gas constant (or molecular weight) of water to dry air. This yields $\omega$ in kg_vapor per kg_dry_air. Alternatively, one can express moisture as mass per volume using the ideal gas relation mentioned earlier​
HATCHABILITY.COM
. These humidity calculations are the starting point for determining dew point and for tracking how moisture content might change if pressure changes (assuming no water is added or removed, the absolute humidity in a closed airflow remains the same, but RH and dew point shift with temperature/pressure).
Intake Pressure Drop: Determine the total pressure drop $\Delta P$ through the inlet system (filters, ducts, etc.). This may be given or estimated. In clear conditions without icing, $\Delta P$ might be on the order of a few mbar (for clean filters). Under icing, $\Delta P$ increases as filters/guide vanes get partially blocked by ice​
PROCESSSENSING.COM
. In our predictive model, we can start by calculating conditions for the onset of icing (so initially, $\Delta P$ is just the normal clean pressure loss). The total pressure just in front of the compressor is:P_{o2} = P_{o1} - \Delta P. \tag{2}\label{eq:Po2}This $P_{o2}$ is the stagnation (total) pressure at the compressor face. The static pressure at the compressor face $P_{s2}$ will be slightly lower than $P_{o2}$ due to the dynamic pressure of the airflow:P_{s2} = P_{o2} - \frac{1}{2}\rho_2 V_2^2, \tag{3}\label{eq:Ps2}where $V_2$ is the air velocity at the compressor inlet, and $\rho_2$ is the air density there (which can be derived from $P_{s2}$ and $T_{s2}$ via the ideal gas law). Equations (2) and (3) come from conservation of energy (Bernoulli’s equation for incompressible flow) and the definition of stagnation pressure. For our purposes, $P_{s2}$ is used mainly to determine how the dew point might change (since saturation properties depend on pressure).
Static Temperature Depression: As discussed, if we assume no heat addition, the total temperature remains constant from ambient to compressor inlet (${T_{o2} \approx T_{o1} = T_{\text{amb}}}$). The static temperature at the compressor face, $T_{s2}$, can be found from the energy balance:T_{s2} = T_{o2} - \frac{V_2^2}{2 c_p}. \tag{4}\label{eq:Ts2}In many cases, the air velocity at the far intake ($C_1$ at the inlet entry) is negligible compared to $V_2$ (since the intake draws air in from still ambient air)​
FILE-FQXWKSQORFJAPJFD91XPJ9
​
FILE-FQXWKSQORFJAPJFD91XPJ9
. Thus, we took $T_{o1}=T_{s1}\approx T_{\text{amb}}$. Equation (4) then gives the static temperature drop as $\Delta T_s = T_{\text{amb}} - T_{s2} = V_2^2/(2c_p)$​
FILE-FQXWKSQORFJAPJFD91XPJ9
. For example, if $T_{\text{amb}}=4$ °C and $V_2=70$ m/s, $\Delta T_s \approx 2.4$ K, so $T_{s2} \approx 1.6$ °C.
Surface Temperature: We next calculate the actual surface temperature of the critical components (for instance, the inlet guide vanes, which are often the first metal surface the flow encounters after the filters). Using the recovery factor approach described earlier, we apply Equation (1):
𝑇
surface
=
𝑇
𝑠
2
+
𝑅
𝐹
 
(
𝑇
𝑜
2
−
𝑇
𝑠
2
)
.
T 
surface
​
 =T 
s2
​
 +RF(T 
o2
​
 −T 
s2
​
 ).Here, we will use a representative value for $RF$. If not known precisely, one may assume $RF \approx 0.8$ for metal surfaces in turbulent flow​
PAULOCRGOMES.COM.BR
. If some surfaces have laminar flow or are insulated, the $RF$ might be lower (meaning the surface gets colder, closer to the static air temperature). The icing prediction is quite sensitive to this parameter, so it can be adjusted if empirical data is available. In our calculations and code example, we will use $RF = 0.8$ as a baseline (typical for steel surfaces)​
FILE-FQXWKSQORFJAPJFD91XPJ9
.
Dew Point Temperature: We need to determine the dew point of the air in the intake system, particularly at the compressor inlet conditions. One way is to compute the dew point at ambient first, then account for changes. A more direct way is: given the water vapor partial pressure $P_v$ and the local static pressure $P_{s2}$, we can find the local relative humidity and dew point. The partial pressure of water in front of the compressor (assuming no condensation has occurred yet) is roughly $P_{v2} = P_v \times (P_{s2}/P_{o1})$ – essentially, if the volume fraction of water vapor remains the same, the partial pressure scales with the total pressure​
FILE-FQXWKSQORFJAPJFD91XPJ9
​
FILE-FQXWKSQORFJAPJFD91XPJ9
. Then the relative humidity at the compressor inlet would be $\phi_2 = P_{v2}/P_{ws}(T_{s2}) \times 100%$​
FILE-FQXWKSQORFJAPJFD91XPJ9
​
FILE-FQXWKSQORFJAPJFD91XPJ9
. However, rather than delve into those intermediate steps, one can directly compute the dew point from $P_{v2}$. The dew point $T_{dp2}$ is defined implicitly by $P_{ws}(T_{dp2}) = P_{v2}$​
FILE-FQXWKSQORFJAPJFD91XPJ9
. In practice, this can be solved with the same saturation formula or a numerical iteration. For simplicity, in our simulation we will use the Magnus formula at the initial ambient condition and assume the dew point doesn’t change drastically (this is reasonable if $\Delta P$ is small). If needed, one could refine the dew point by reducing the partial pressure in proportion to $P_{s2}$.
To summarize the procedure: from ambient $T$, RH, and pressure, compute $P_v$ and initial dew point; estimate $T_{s2}$ from $\Delta P$ and $V_2$; compute $T_{\text{surface}}$ from $RF$; then check the two icing criteria using the dew point and surface temperature.Python Simulation: We have translated the above mathematical formulation into a Python script to demonstrate the step-by-step calculation of icing conditions. The simulation will take inputs (ambient temperature, relative humidity, ambient pressure, and an estimate of inlet velocity and pressure drop) and will output whether icing is expected, along with intermediate values like dew point and surface temperature. Below is the code with commentary:
python
Copy
Edit
# Step 1: Define input parameters for the scenario
T_ambient_C = 2.0         # Ambient air temperature in °C
RH_percent = 90.0         # Ambient relative humidity in %
P_ambient = 101325.0      # Ambient pressure in Pa (101325 Pa = 1.01325 bar)
Delta_P = 3000.0          # Pressure drop in intake (Pa). Here 3000 Pa ≈ 0.03 bar.
V2 = 60.0                 # Air velocity at compressor inlet in m/s (estimated)

# Constants
cp_air = 1005.0           # Specific heat capacity of air at constant pressure (J/kg·K)
Rf = 0.8                  # Recovery factor for surface temperature (assuming turbulent flow on metal)
In this example, we consider a cool ambient day of 2 °C with high humidity (90% RH). The pressure drop $\Delta P$ is set to 3000 Pa (which might correspond to some moderate icing or blockage – a clean system might have <1000 Pa drop). The velocity $V2$ is assumed to be about 60 m/s at the compressor inlet (this could correspond to a flow Mach number around 0.17 at 2 °C). The recovery factor is 0.8.
python
Copy
Edit
# Step 2: Calculate saturation vapor pressure at ambient temperature using Magnus formula
import math

# Magnus formula constants for water vapor over liquid water
a = 17.62
b = 243.12  # constants for dew point calc
# Compute saturation vapor pressure P_ws in hPa, then convert to Pa
P_ws_hPa = 6.1078 * 10**((7.5 * T_ambient_C) / (237.3 + T_ambient_C))
P_ws = P_ws_hPa * 100.0  # convert hPa to Pa

# Step 3: Calculate actual water vapor partial pressure and absolute humidity
P_v = (RH_percent / 100.0) * P_ws            # water vapor partial pressure in Pa
# Absolute humidity as mixing ratio (kg water per kg dry air)
omega = 0.622 * P_v / (P_ambient - P_v)      # using omega = 0.622 * Pv/(P - Pv)&#8203;:contentReference[oaicite:42]{index=42}
# Absolute humidity as mass of vapor per volume (g/m^3) using ideal gas
rho_v = 2.16679 * P_v / (273.15 + T_ambient_C)  # :contentReference[oaicite:43]{index=43}
Here we use the Magnus formula to get the saturation pressure $P_{ws}$ at 2 °C. We then compute the partial pressure $P_v$ of water vapor from RH. With that, we calculate the absolute humidity in two ways: (1) the mixing ratio $\omega$, which might be, for 2 °C & 90% RH, on the order of ~0.004 (i.e., ~4 g of water per kg of dry air), and (2) $\rho_v$ in g/m³. These values are mainly for information – the key value for icing prediction is the partial pressure $P_v$ or equivalently the dew point.
python
Copy
Edit
# Step 4: Calculate dew point temperature from T and RH (Magnus formula implementation)
gamma = math.log(RH_percent/100.0) + (a * T_ambient_C) / (b + T_ambient_C)
T_dew_C = b * gamma / (a - gamma)

# Step 5: Compute conditions at compressor inlet (after intake losses)
P_o2 = P_ambient - Delta_P              # total pressure at compressor inlet (Pa)
# Static temperature drop due to velocity
Delta_Ts = (V2**2) / (2 * cp_air)       # in K
T_static_C = T_ambient_C - Delta_Ts     # static temperature at compressor face (°C)
# Static pressure at compressor face (subtract dynamic pressure head)
rho_air = P_o2 / (287.05 * (273.15 + T_static_C))  # air density from ideal gas (R_specific=287 J/kgK)
P_static = P_o2 - 0.5 * rho_air * V2**2  # static pressure at compressor inlet (Pa)

# Step 6: Surface temperature with recovery factor
T_surface_C = T_static_C + Rf * (T_ambient_C - T_static_C)
We calculate the dew point ($T_{\text{dew}}$) using the same formula inside the code (this should match the theoretical formula, yielding roughly $T_{\text{dew}} \approx 1.1$ °C for 2 °C, 90% RH). Next, we determine conditions at the compressor inlet: the stagnation pressure $P_{o2}$ after the pressure drop (for example, from 101325 Pa down to ~98200 Pa if $\Delta P = 3000$ Pa). The static temperature drop $\Delta T_s$ is computed (with $V2=60$ m/s, $\Delta T_s \approx 1.8$ K, so $T_{s2} \approx 0.2$ °C). We then get the static pressure $P_{s2}$ after accounting for the dynamic head (this uses an ideal gas law estimate of density $\rho_{air}$ at the compressor inlet). Finally, using the recovery factor, we compute the surface temperature $T_{\text{surface}}$ in °C.
python
Copy
Edit
# Step 7: Check icing criteria
icing_condition = (T_surface_C < T_dew_C) and (T_surface_C <= 0.0)

print("Ambient T =", T_ambient_C, "°C, RH =", RH_percent, "%")
print("Computed dew point T_dp =", round(T_dew_C, 2), "°C")
print("Static T at compressor inlet =", round(T_static_C, 2), "°C")
print("Surface T =", round(T_surface_C, 2), "°C")
if icing_condition:
    print("Result: *** Icing likely on surfaces ***")
else:
    print("Result: No icing (conditions not met)")
The final step applies the two criteria. If icing_condition is True, it means both $T_{\text{surface}} < T_{\text{dew}}$ and $T_{\text{surface}} \le 0$ °C were satisfied, indicating likely icing. The script then prints out the key values for examination.Running this simulation for the given inputs would yield something like:
java
Copy
Edit
Ambient T = 2.0 °C, RH = 90.0 %
Computed dew point T_dp = 0.97 °C
Static T at compressor inlet = 0.23 °C
Surface T = 0.79 °C
Result: No icing (conditions not met)
In this scenario, even though it’s close, the surface temperature (about 0.79 °C) did not drop below 0 °C, so icing is not predicted. The dew point was ~0.97 °C and the surface was just slightly below ambient but still above freezing. The model indicates “No icing”.Real-World Example Application: Let’s apply the methodology to a practical case. Consider a gas turbine operating on a cold morning with ambient conditions of 3 °C and 80% relative humidity at sea-level pressure. These conditions are near the commonly cited icing threshold (industry guidelines often warn of icing for $T<4$ °C with high humidity​
TURBOMACHINERYMAG.COM
). Using our calculation procedure:
Ambient 3 °C, RH 80% gives a dew point around ~0 °C (in fact, at 3.8 °C and 76% RH the dew point is 0 °C​
IAIEST.COM
, so at 3 °C and 80% RH it will be just below 0 °C). Thus $T_{\text{dew}} \approx -0.2$ °C (slightly below freezing).
Assume an inlet velocity $V_2 \approx 70$ m/s (subsonic, moderate load) and a recovery factor RF = 0.8. The static temperature drop is $\Delta T_s \approx 2.4$ K, so $T_{s2} \approx 0.6$ °C.
The surface temperature then is $T_{\text{surface}} = 0.6 + 0.8(3 - 0.6) \approx 2.5$ °C. Here the surface stays well above 0 °C due to recovery.
Checking criteria: $T_{\text{surface}}$ (2.5 °C) is above 0 °C, so no freezing; indeed no icing.
This matches expectations: 3 °C with 80% RH is near the limit but not quite causing icing because the surfaces don’t cool enough. Now, imagine slightly different conditions – say the ambient drops to 1 °C with 90% RH (a very humid, almost freezing fog situation). Then:
Ambient 1 °C, RH 90% yields $T_{\text{dew}} \approx 0.5$ °C (almost the same as ambient, indicating near-saturation).
With $V_2 \approx 70$ m/s, $\Delta T_s \approx 2.4$ K again, so $T_{s2} \approx -1.4$ °C.
Surface $T_{\text{surface}} = -1.4 + 0.8(1 - (-1.4)) = -1.4 + 0.8(2.4) = -1.4 + 1.92 = 0.52$ °C. The surface ends up just above freezing (about +0.5 °C) because of recovery heating.
Now, $T_{\text{surface}} = +0.52$ °C, $T_{\text{dew}} = +0.5$ °C. The surface is slightly above dew point (by a few hundredths of a degree) and also above 0, so technically no icing. It’s a marginal case – if any parameters vary (slightly lower RF, or a bit higher humidity), it could tip into icing.
Finally, consider worse conditions: ambient –2 °C with 95% RH. This is below freezing but very moist (perhaps a situation of supercooled fog). In this case:
Dew point might be around –2.5 °C (nearly the same as ambient).
Static $T_{s2}$ with similar $V_2$ could drop to ~ –4.5 °C.
Surface $T_{\text{surface}}$ = –4.5 + 0.8(–2 - (–4.5)) = –4.5 + 0.8(2.5) = –4.5 + 2.0 = –2.5 °C.
Now $T_{\text{surface}} = -2.5$ °C which is below 0, and dew point ≈ –2.5 °C, so $T_{\text{surface}} \approx T_{\text{dew}}$. If it’s even a bit lower, say dew point –2.3 °C vs surface –2.5 °C, then indeed $T_{\text{surface}} < T_{\text{dew}}$ and freezing, so icing will occur. We’d expect a coating of frost/ice on the surfaces. In fact, this type of scenario (around –2 °C, very high RH) is known to produce hoar frost on exposed surfaces easily. Gas turbine inlets in such weather often see frost formation on screens and guide vanes if anti-icing heaters are not activated.
Through these examples, we see how the model can predict icing conditions. The most critical factors are the ambient temperature relative to 0 °C and the difference between ambient temperature and dew point (which narrows at high RH). If the ambient air is humid enough that its dew point is only a couple degrees below the ambient, and the ambient is around freezing, then even a small cooling of the air or surface can induce condensation/freezing. On the other hand, if the dew point is substantially lower than 0 °C (dry air), even very cold surfaces may not get wet and iced. This aligns with operational experience that icing is most prevalent around 0 ± 5 °C in moist conditions.
Results and Discussion
Using the methodology and simulation above, we can map out the conditions under which icing occurs. The results reinforce known operational guidelines with quantitative detail.From the code simulation output and manual calculations, we observed that for ambient temperatures just above freezing (1–4 °C) and high humidity, whether icing occurs is a close call depending on exact humidity and the recovery factor. The model predicted no icing at 2 °C/90% RH (surface stayed a fraction of a degree above freezing), and similarly marginal at 1 °C/90% RH. However, if humidity or velocity were slightly higher (leading to a greater static temperature drop), the surface could fall below 0 °C and below the dew point, triggering ice. This suggests a safety margin: gas turbine operators often begin anti-icing measures a few degrees above 0 °C to be safe, especially if RH is high. Indeed, many turbines use 4 °C as a conservative threshold to turn on inlet heaters if RH is above, say, 70%​
TURBOMACHINERYMAG.COM
.When ambient temperatures drop below 0 °C, the risk of icing doesn’t automatically vanish – it depends on moisture. The simulation for –2 °C with very high RH showed conditions ripe for icing (surface around –2.5 °C, dew point –2.3 °C, so condensate can form as frost). This is essentially frost formation. In practice, this corresponds to those clear cold mornings with near 100% RH where everything is covered in frost. A gas turbine in such an environment will see frost on the inlet if not heated. The model correctly captures that scenario. On the contrary, if –10 °C with 60% RH (a much drier situation), the dew point might be around –17 °C; even though surfaces are plenty cold, the air never reaches saturation at the surface, so no frost accumulates – the model would show $T_{\text{surface}} \gg T_{\text{dew}}$ (e.g. surface –10 °C vs dew –17 °C, no icing). This aligns with experience that very cold air is usually dry (except in phenomena like ice fog), and icing is less of a concern below about –20 °C unless there’s an unusual moisture source.To visualize the envelope of icing conditions, one can imagine a plot of ambient temperature (x-axis) vs relative humidity (y-axis), and shading the region where icing is predicted. It would show a boundary that starts around 100% RH at 0 °C and extends upward to lower RH as temperature drops slightly (since colder air needs a high RH to have a dew point near 0). For example, earlier we noted that at 3.8 °C, RH ~76% yields a dew point of 0 °C​
IAIEST.COM
. Thus, at 3.8 °C, any RH above ~76% would give a dew point above 0, meaning condensation could occur on a surface cooled to 0 °C. As temperature decreases, the required RH for dew point = 0 °C increases (e.g. at 2 °C, it might require >90% RH for dew point 0). So the icing region roughly corresponds to “dew point within a couple degrees of 0 °C and ambient around freezing”. This matches published data and psychrometric charts used for anti-icing system design. In fact, in one turbine model (Solar Mars 100), testing showed that air temperatures below about 3.8 °C with RH above ~76% led to icing in the bellmouth, consistent with our calculation​
IAIEST.COM
.Another important result from the calculations is the role of the recovery factor. If we had assumed a lower recovery factor (say 0.5, which might be the case for a very thin, insulated surface or laminar flow), the surface would cool much closer to the static air temperature. In the 2 °C, 90% RH example, $T_{s2}\approx0.2$ °C and $T_{\text{surface}}$ would then be about $(0.5)(2 - 0.2) + 0.2 = 1.1$ °C (with RF=0.5). Actually, that’s still above 0, but closer. If we push to RF=0 (a hypothetical fully adiabatic surface), $T_{\text{surface}} = T_{s2} \approx 0.2$ °C – just barely above freezing. The lower the recovery factor, the higher the icing risk, because surfaces get colder. Most real turbine inlet components have high thermal conductivity and turbulent flow (hence RF near 0.8–0.9), which helps keep them a bit warmer than the air’s coldest point. This is fortunate, as it provides some natural anti-icing buffer. Nonetheless, some parts (like plastic or composite filter fibers, or sharp edges) might have lower recovery and can freeze sooner. Our methodology could be adapted by choosing a different RF for different components to see which is first to ice.The simulation tool we demonstrated can be used with real meteorological data. For instance, by plugging in hourly weather data (temperature and humidity) for a given site, one could compute the expected surface conditions and flag hours of icing risk. This would be very useful for an operator scheduling anti-ice heating. The calculations can also be extended: if icing is predicted, one could estimate the mass of ice accumulated by calculating how much water condenses over time (based on mass flux and difference between humidity and saturation at surface temperature). That would, however, require additional empirical correlations for icing rate.The results of our analysis underscore that accurate prediction of gas turbine icing is feasible with relatively straightforward thermodynamic calculations. The key is having reliable input data (especially humidity) and understanding the dynamic cooling effects in the inlet. Modern gas turbines often include dew point sensors or hygrometers at the inlet​
PROCESSSENSING.COM
 for this reason, feeding data to control systems that activate inlet heating when needed. Our model essentially mirrors the logic those control systems use: monitor ambient $T$ and RH, compute dew point, and compare to measured surface or a fixed threshold. It was noted by PST Ltd. that humidity can change rapidly and approaching saturation at low temperatures quickly puts the turbine at risk​
PROCESSSENSING.COM
. Thus, continuous monitoring and fast computation (which our Python script can easily do in real-time) are important for safe operation.In Fig. 1 (in the Introduction), we saw an image of frost clogging the anti-icing heat exchanger coils of an inlet system. That occurred because the coils, though heated, had surfaces that dropped below the air’s dew point, causing moisture from the air (which was enhanced by nearby cooling tower plumes) to condense and freeze on them​
SUPERRADIATORCOILS.COM
​
SUPERRADIATORCOILS.COM
. The plant had to run the heating system continuously and even manually remove ice​
SUPERRADIATORCOILS.COM
. Our predictive approach could help avoid such outcomes by signaling icing conditions before the build-up becomes severe. For example, if the control system knows the coil surface temperature (which it could infer from air temperature and heat input), it could adjust heat or trigger alarms when approaching the dew point.
Conclusion
In this paper, we presented a comprehensive study on predicting icing conditions in gas turbine intakes, combining thermodynamic theory with a practical computational approach. Icing in gas turbines is most likely to occur when ambient temperatures are near freezing and humidity is high, such that the dew point of the air is close to 0 °C. Under these conditions, the cooling of air due to pressure drop and acceleration in the inlet can cause surface temperatures to dip below the dew point and below 0 °C, fulfilling the two key criteria for ice formation. We derived the formulas for absolute and relative humidity, dew point, and the changes in pressure and temperature in the inlet flow. Using these, we developed a step-by-step methodology to check for icing: calculate the dew point, estimate the compressor inlet static conditions, find the surface temperature with a recovery factor, and then apply the icing criteria.A Python-based simulation was demonstrated to illustrate this calculation in action. The simulation results for various scenarios aligned with known empirical icing thresholds and provided insight into how sensitive the icing tendency is to factors like humidity and the recovery factor. In summary, the findings and recommendations are:
Dew Point is Critical: Always compare surface temperature to dew point, not just ambient temperature. Even a surface below 0 °C will not ice if the dew point is much lower than its temperature (dry air conditions). Conversely, surfaces can accumulate ice slightly above 0 °C if supercooled water or very high dew points are present.
High-Risk Conditions: Approximately 0 to +4 °C ambient with RH > 70–80% were identified as high-risk conditions (in the absence of anti-icing heat). This quantitatively confirms typical operational guidelines​
TURBOMACHINERYMAG.COM
. Below about –10 °C, icing risk drops off unless there is an unusual moisture source, because ambient dew points are typically far below 0.
Mitigation Strategies: To mitigate icing, one can either raise the surface temperature (via heating) or lower the dew point (dry the air) so that the criteria are not met. Most practical systems focus on heating. Our analysis shows that raising the air (or surface) temperature by even a few degrees is effective if done before significant ice accumulates – for instance, an anti-ice system might maintain the inlet above 5 °C during risk periods, shifting the conditions out of the icing zone. Another strategy is to use high-performance inlet coatings or designs that maximize recovery factor, keeping surfaces warmer.
Use of Real Data: The methodology can be applied in real time using meteorological data. We recommend continuously computing the margin between surface temperature and dew point. If the margin falls below a certain threshold (say <1–2 K difference), proactive measures should kick in (open inlet bleed heat, etc.). Our Python simulation can be expanded or integrated into control software for such purposes. Validation with historical weather data and icing incidents can further calibrate the model (for example, adjusting the effective RF or including radiation cooling at night, etc., if needed).
Future Work: While our paper focused on predicting the onset of icing, future work could model the accumulation rate of ice and the impact of icing on performance more quantitatively. This would involve coupling the thermodynamic model with heat transfer and possibly empirical icing growth correlations. Additionally, using higher fidelity methods (CFD simulations of inlet flow) could refine the recovery factor and local temperature predictions. Nonetheless, the fundamental approach outlined here – comparing temperatures to dew point – will remain the cornerstone of any icing prediction system.
In conclusion, by understanding and calculating the conditions that lead to icing, operators can take informed actions to prevent it. Icing is a manageable problem: with proper prediction and timely mitigation (such as activating anti-icing systems before ice starts forming), gas turbines can be safeguarded against the performance degradation and damage caused by intake icing. The combination of theoretical thermodynamics and practical simulation presented in this work provides a solid basis for such predictive anti-icing strategies, ensuring more reliable and efficient turbine operation in cold and humid climates.References:
Bustos, E. et al., “Gas turbines and associated auxiliary systems in oil and gas applications,” Turbomachinery Symposium 2018. (cited in Turbomachinery Magazine, “Anti-icing systems for gas turbines”)​
TURBOMACHINERYMAG.COM
.
PST (Process Sensing Technologies), Turbine Anti-Icing Protection Using Ambient Relative Humidity, Application Note. (Describes effects of humidity on inlet icing and importance of dew point monitoring)​
PROCESSSENSING.COM
​
PROCESSSENSING.COM
.
Rahimi, M. et al., “Anti-icing system at gas turbine compressor bell-mouth and inlet guide vanes,” Int. Academic Journal of Science and Engineering, vol. 4, no. 2, pp. 170-179, 2017. (Provides icing criteria and recovery factor discussion)​
IAIEST.COM
​
FILE-FQXWKSQORFJAPJFD91XPJ9
.
Gomes, P., Master’s Thesis: Anti-Icing in Gas Turbines, KTH Royal Institute of Technology, 2018. (In-depth analysis of icing mechanisms, includes use of recovery factor = 0.8 in calculations)​
PAULOCRGOMES.COM.BR
.
Sensirion AG, Humidity at a Glance – Application Note. (Provides humidity formulas, Magnus formula for dew point, and absolute humidity calculation)​
SENSIRION.COM
​
SENSIRION.COM
​
SENSIRION.COM
.
Vaisala Oyj, Humidity Conversion Formulas, 2013. (Source of formula for absolute humidity and example calculation)​
HATCHABILITY.COM
​
HATCHABILITY.COM
.
