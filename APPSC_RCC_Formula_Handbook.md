# APPSC Assistant Professor Screening Test — RCC Formula Handbook
## Reinforced Cement Concrete (RCC): High-Value Formulas and Simple Examples

> Study note: This is a broad revision handbook based on standard RCC/structural mechanics concepts. Exact design calculations must follow the relevant edition of IS 456, IS 10262, IS 875, IS 1786 and other applicable standards, and the APPSC syllabus. Formula applicability and coefficients can vary by code clause and assumptions. Examples below are educational, not construction designs.

## 1. Basic material and unit formulas

### 1.1 Stress
\[
\sigma=\frac{P}{A}
\]
Stress = force / resisting area. Example: if Baahubali pushes a short concrete prism with 200,000 N over 10,000 mm², average stress = 20 N/mm².

### 1.2 Strain
\[
\varepsilon=\frac{\Delta L}{L}
\]
Strain = change in length / original length, no unit. If a 2,000 mm bar lengthens by 1 mm, strain = 1/2000 = 0.0005.

### 1.3 Young's modulus
\[
E=\frac{\sigma}{\varepsilon}
\]
For concrete, IS 456 gives the commonly used short-term estimate \(E_c=5000\sqrt{f_{ck}}\) MPa for normal-weight concrete. If \(f_{ck}=25\) MPa, \(E_c=5000\sqrt{25}=25,000\) MPa. Use the code formula only within its intended scope.

### 1.4 Unit weight and self-weight
\[
W=\gamma V
\]
Self-weight = unit weight × volume. A concrete slab of volume 2 m³ at an assumed unit weight of 25 kN/m³ weighs about 50 kN.

### 1.5 Load conversion
\[
1\text{ kN}=1000\text{ N},\qquad 1\text{ MPa}=1\text{ N/mm}^2
\]
Before calculating, keep units consistent.

## 2. RCC design concepts and notation
- \(f_{ck}\): characteristic compressive strength of concrete at 28 days (MPa).
- \(f_y\): characteristic yield strength of reinforcing steel (MPa).
- \(b\): beam breadth; \(D\): overall depth; \(d\): effective depth.
- \(A_{st}\): area of tension reinforcement; \(A_{sc}\): compression steel area.
- \(M_u\): factored bending moment; \(V_u\): factored shear force; \(P_u\): factored axial load.
- Limit State Design (LSD) is the principal method in IS 456:2000. Do not confuse limit-state design formulas with historical Working Stress Method formulas.

## 3. Flexure of singly reinforced rectangular beams — IS 456 limit-state framework

### 3.1 Lever arm
\[
z=d-0.42x_u
\]
For the standard rectangular stress block in the applicable singly reinforced limit-state analysis, where \(x_u\) is neutral-axis depth.

### 3.2 Ultimate moment of resistance
\[
M_u=0.36f_{ck}b x_u(d-0.42x_u)
\]
Also expressed as:
\[
M_u=0.87f_yA_{st}(d-0.42x_u)
\]
Use the compatible stress-block and equilibrium assumptions and ensure equilibrium between compression and tension forces.

### 3.3 Neutral-axis depth from force equilibrium
\[
0.36f_{ck}b x_u=0.87f_yA_{st}
\]
Hence:
\[
x_u=\frac{0.87f_yA_{st}}{0.36f_{ck}b}
\]

### 3.4 Limiting neutral-axis depth
For common IS 456 design grades:
- Fe 250: \(x_{u,max}/d=0.53\)
- Fe 415: \(x_{u,max}/d=0.48\)
- Fe 500: \(x_{u,max}/d=0.46\)

Check the current standard and steel grade rather than memorising this list blindly.

### 3.5 Limiting moment of resistance (singly reinforced section)
\[
M_{u,lim}=R_{lim}f_{ck}bd^2
\]
Common coefficients derived from IS 456 stress block:
- Fe 250: approximately \(0.149f_{ck}bd^2\)
- Fe 415: approximately \(0.138f_{ck}bd^2\)
- Fe 500: approximately \(0.133f_{ck}bd^2\)

Use matching units: MPa × mm × mm² = N·mm, then divide by \(10^6\) for kN·m.

### 3.6 Tension steel from moment (preliminary)
\[
A_{st}\approx\frac{M_u}{0.87f_y z}
\]
This is a useful equilibrium-based sizing expression where the design assumptions are appropriate; calculate/check \(x_u\), ductility, minimum/maximum steel and detailing separately.

**Baahubali example:** A palace-floor beam sags under the crowd. Concrete mainly carries compression at the top and steel bars resist tension at the bottom. The lever arm \(z\) is the distance between these force resultants, enabling a resisting couple.

## 4. Minimum and maximum longitudinal reinforcement in beams

### 4.1 Minimum tension reinforcement
\[
A_{st,min}=\frac{0.85bd}{f_y}
\]
(Use dimensions in mm and \(f_y\) in MPa.) This is the familiar IS 456 minimum reinforcement expression for beams.

### 4.2 Maximum tension reinforcement
\[
A_{st,max}=0.04bD
\]
Common IS 456 beam limit for tension reinforcement; verify detailing provisions and the applicable code edition.

**Baahubali example:** A beam needs enough bars to resist bending but not so many that concrete cannot be placed and compacted properly.

## 5. Shear in RCC beams

### 5.1 Nominal shear stress
\[
\tau_v=\frac{V_u}{bd}
\]
where \(V_u\) is the shear force at the relevant section. Units are N/mm² if \(V_u\) is N and dimensions are mm.

### 5.2 Percentage tension steel
\[
p_t=\frac{100A_{st}}{bd}
\]
Use this with the applicable code table to obtain concrete design shear strength \(\tau_c\).

### 5.3 Vertical stirrup contribution
\[
V_{us}=\frac{0.87f_yA_{sv}d}{s}
\]
for vertical stirrups within the relevant IS 456 design assumptions, where \(A_{sv}\) is total cross-sectional area of stirrup legs in one spacing and \(s\) is spacing.

### 5.4 Required stirrup spacing (from the simplified expression)
\[
s=\frac{0.87f_yA_{sv}d}{V_{us}}
\]
Check maximum spacing, minimum shear reinforcement and maximum shear stress provisions separately.

**Baahubali example:** Near a beam support, diagonal cracking can occur. Stirrups act like hoops that cross and help resist diagonal tension; they are not a substitute for checking concrete shear capacity.

## 6. Development length, anchorage and bond

### 6.1 Development length
\[
L_d=\frac{\phi\,\sigma_s}{4\tau_{bd}}
\]
For the usual limit-state development-length expression, \(\phi\) is bar diameter, \(\sigma_s\) is stress in bar at the section (often taken as \(0.87f_y\) when the bar is at design stress), and \(\tau_{bd}\) is design bond stress from the code.

### 6.2 Common form when the bar stress is taken as 0.87fy
\[
L_d=\frac{\phi(0.87f_y)}{4\tau_{bd}}
\]
Bond stress increases for deformed bars and is modified for bars in compression according to code rules. Always consult the relevant table and clause.

**Baahubali example:** Steel bars must be anchored far enough into a column or beam joint so they do not pull out when the palace frame is loaded.

## 7. Slabs

### 7.1 One-way or two-way action
- If the ratio of longer span to shorter span \(L_y/L_x>2\), a simply supported slab generally acts as one-way.
- If \(L_y/L_x\le 2\) and supported on four sides, two-way action may apply, subject to support and boundary conditions.

### 7.2 One-way slab bending moment (simply supported, uniformly distributed load)
\[
M=\frac{wL^2}{8}
\]
For a one-metre design strip, take \(w\) as load per metre width and \(L\) as effective span; use the applicable load combination/design basis.

### 7.3 Cantilever slab/strip bending moment under uniform load
\[
M=\frac{wL^2}{2}
\]
At the fixed support (magnitude), for uniformly distributed load over the full cantilever length.

### 7.4 Two-way slab moment
\[
M_x=\alpha_x wL_x^2,\qquad M_y=\alpha_y wL_x^2
\]
Use the appropriate coefficient table, panel aspect ratio, support conditions and code provisions; do not invent coefficients.

### 7.5 Effective depth
\[
d=D-\text{nominal cover}-\text{half bar diameter}
\]
For a single bottom layer; adjust for actual bar arrangement.

### 7.6 Slab minimum reinforcement (IS 456 general rule)
- Mild steel: 0.15% of gross cross-sectional area.
- High-strength deformed bars: 0.12% of gross cross-sectional area.
\[
A_{s,min}=\frac{p}{100}bD
\]
Use the specified percentage and check spacing/maximum bar diameter limits.

**Baahubali example:** A palace hall floor spreads crowd load toward supports. A one-way slab mainly spans in the short direction; a two-way slab shares bending in both directions.

## 8. Columns

### 8.1 Short tied column axial capacity (simplified IS 456 expression)
\[
P_u=0.4f_{ck}A_c+0.67f_yA_{sc}
\]
where \(A_c\) is area of concrete excluding longitudinal steel and \(A_{sc}\) is longitudinal steel area, for the specified short axially loaded tied-column conditions and minimum eccentricity assumptions. This is not a universal formula for all columns.

### 8.2 Longitudinal reinforcement ratio (common column limits)
\[
0.8\%\le\frac{A_{sc}}{A_g}\times100\le6\%
\]
Common IS 456 limits; practical detailing, lap locations and congestion can further govern. Check the code.

### 8.3 Slenderness ratios
\[
\lambda_x=\frac{l_{ex}}{D_x},\qquad \lambda_y=\frac{l_{ey}}{D_y}
\]
Effective length divided by corresponding lateral dimension. Column classification and moment magnification depend on the code definition and restraints.

### 8.4 Minimum eccentricity (IS 456 form)
\[
e_{min}=\frac{l}{500}+\frac{D}{30},\quad \text{but not less than }20\text{ mm}
\]
Use the relevant unsupported length and cross-sectional dimension as prescribed. Do not treat a column as perfectly concentrically loaded in design.

### 8.5 Helical reinforcement pitch (detailing)
Pitch limits and volumetric ratio are prescribed by IS 456; use the relevant clause rather than a generic capacity formula. Confirm minimum/maximum pitch and end detailing.

**Baahubali example:** A palace column carries floor and roof loads downward. If it is too slender, it may bow sideways (buckling) even before the concrete reaches its crushing strength. Axial capacity alone is not enough.

## 9. Bond, cover and detailing

### 9.1 Clear cover
Clear cover is measured from the concrete surface to the outer surface of reinforcement (including links where they enclose main bars). Required cover depends on exposure, fire and member type; use the applicable code table.

### 9.2 Bar spacing
Spacing is a code detailing check. Minimum clear spacing must permit concrete and aggregate to pass and allow compaction. Follow IS 456 detailing clauses and bar diameter/aggregate constraints.

### 9.3 Lap length
Lap lengths depend on whether the bar is in tension or compression and the relevant code provisions. Use development length and IS 456 lap rules; do not memorise one single value for every situation.

## 10. RCC working stress method (historical method)

The Working Stress Method uses service/working loads and permissible stresses. It is distinct from the limit-state expressions above.

### 10.1 Elastic bending relationship
\[
\frac{M}{I}=\frac{\sigma_c}{y_c}=\frac{\sigma_s}{m y_s}
\]
where \(m=E_s/E_c\) is the modular ratio in the elastic transformed-section approach, and symbols should be defined for the section being analysed.

### 10.2 Modular ratio — historical IS 456 working-stress expression
\[
m=\frac{280}{3\sigma_{cbc}}
\]
This is a historical WSM expression associated with permissible bending compressive stress in concrete. Confirm the exact code edition and context before using it in an exam answer.

### 10.3 Neutral axis and transformed section
For a cracked singly reinforced rectangular section under classical WSM, neutral-axis depth \(x\) is obtained from the transformed-section equilibrium relationship. A commonly used expression, where \(b\) is width, \(d\) effective depth, \(m\) modular ratio and \(A_{st}\) tension steel area, is:
\[
\frac{b x^2}{2}=mA_{st}(d-x)
\]
Use only under the stated cracked-section, elastic assumptions.

### 10.4 WSM stress checks
\[
\sigma_c\le\sigma_{cbc},\qquad \sigma_s\le\sigma_{st}
\]
where allowable values depend on the applicable code and loading/stress case. Do not use the simplified yield-stress/FOS relationship blindly for RCC concrete design.

## 11. Torsion in RCC beams
IS 456 uses equivalent shear and equivalent bending concepts for design where torsion is significant. The expressions and reinforcement detailing are clause-specific; learn them from the exact code/syllabus version rather than mixing them with generic formulas.

## 12. Serviceability checks

### 12.1 Span/depth ratio (basic IS 456 rule of thumb)
Basic span/effective-depth ratios for deflection control are commonly taken as:
- Cantilever: 7
- Simply supported: 20
- Continuous: 26

Modification factors based on tension/compression reinforcement and stress are applied as provided by the code. These are not absolute maximum span values.

### 12.2 Crack control
Crack width and detailing depend on bar spacing, cover, steel stress, exposure and the relevant code requirements. Use the code equations/tables applicable to the problem; do not use a single universal crack-width formula for all cases.

**Baahubali example:** The palace floor should not just avoid collapse; it should also avoid excessive sagging and cracking that damage finishes or make occupants uncomfortable.

## 13. Loads and structural analysis formulas often used with RCC

### 13.1 Simply supported beam with central point load
\[
M_{max}=\frac{PL}{4},\qquad R_A=R_B=\frac{P}{2}
\]

### 13.2 Simply supported beam with uniformly distributed load
\[
M_{max}=\frac{wL^2}{8},\qquad V_{max}=\frac{wL}{2}
\]

### 13.3 Cantilever with point load at free end
\[
M_{support}=PL,\qquad V_{support}=P
\]

### 13.4 Cantilever with full-length UDL
\[
M_{support}=\frac{wL^2}{2},\qquad V_{support}=wL
\]

### 13.5 Bending equation (elastic beam theory)
\[
\frac{M}{I}=\frac{\sigma}{y}=\frac{E}{R}
\]
Use for elastic beam theory, not as a replacement for the IS 456 ultimate limit-state stress block.

### 13.6 Second moment of area — rectangular section
\[
I=\frac{bd^3}{12}
\]
about the centroidal axis parallel to the breadth, for a rectangle.

### 13.7 Section modulus — rectangular section
\[
Z=\frac{I}{d/2}=\frac{bd^2}{6}
\]

## 14. Concrete mix design and basic concrete formulas

### 14.1 Water-cement ratio
\[
w/c=\frac{\text{mass of water}}{\text{mass of cementitious cement as defined in the mix}}
\]
For a basic cement-only illustration, 180 kg water / 360 kg cement = 0.50. Actual mix proportioning follows IS 10262 and durability requirements in IS 456.

### 14.2 Target mean strength (IS 10262 concept)
\[
f'_{ck}=f_{ck}+1.65s
\]
where \(s\) is the standard deviation from the applicable mix-design procedure. The actual code procedure includes criteria for selecting \(s\) and target strength.

### 14.3 Characteristic strength
\[
P(f<f_{ck})\le 5\%
\]
Interpretation: characteristic compressive strength is defined statistically so that not more than 5% of test results are expected below it under the prescribed framework.

### 14.4 Cement content and volume
\[
\text{Mass} = \text{density} \times \text{volume}
\]
For absolute-volume mix design, sum constituent absolute volumes, including water, cementitious materials, aggregates and admixtures as applicable, to meet the batch yield. Follow IS 10262.

## 15. Quick exam memory list
1. Stress: \(P/A\)
2. Strain: \(\Delta L/L\)
3. Concrete modulus estimate: \(5000\sqrt{f_{ck}}\) MPa (within code scope)
4. Flexural moment: \(M=\frac{wL^2}{8}\) for simply supported UDL
5. Slab/beam flexure: \(M_u=0.36f_{ck}b x_u(d-0.42x_u)\)
6. Steel force equilibrium: \(0.87f_yA_{st}=0.36f_{ck}b x_u\)
7. Shear stress: \(\tau_v=V_u/(bd)\)
8. Stirrups: \(V_{us}=0.87f_yA_{sv}d/s\)
9. Development length: \(L_d=\phi\sigma_s/(4\tau_{bd})\)
10. Short axially loaded tied column: \(P_u=0.4f_{ck}A_c+0.67f_yA_{sc}\) under the specified code assumptions
11. Slab minimum reinforcement: generally 0.12% (HYSD) or 0.15% (mild steel), subject to code context
12. WSM stress check: actual stress does not exceed applicable permissible stress

## Study method
Learn one chapter at a time:
1. Memorise symbols and units.
2. Understand the physical meaning using the Baahubali analogy.
3. Work through one numerical example.
4. Solve an MCQ without looking at the answer.
5. Check code clauses/coefficients against the exact standard and your APPSC syllabus.


---

## 16. Baahubali worked examples for the principal formulas

These examples illustrate calculation mechanics only. They are deliberately simplified and must not be used as construction designs. Use the APPSC syllabus and the appropriate code edition for exam-specific conditions.

### A. Stress, strain, modulus and self-weight

**A1. Stress, \(\sigma=P/A\)**  
Baahubali tests a concrete cube-like prism with a load of 180,000 N over a loaded area of 9,000 mm².  
\[
\sigma=180000/9000=20\text{ N/mm}^2
\]  
Meaning: the average compressive stress is 20 MPa.

**A2. Strain, \(\varepsilon=\Delta L/L\)**  
A 2,000 mm steel bar stretches by 1 mm while supporting a palace gate.  
\[
\varepsilon=1/2000=0.0005
\]  
Meaning: the change is small compared with the original length; strain has no unit.

**A3. Concrete modulus estimate, \(E_c=5000\sqrt{f_{ck}}\)**  
For an M25 example, \(E_c=5000\sqrt{25}=25,000\) MPa.  
Meaning: this is the code's empirical estimate for normal-weight concrete within its intended scope, not a measured value for every concrete.

**A4. Self-weight, \(W=\gamma V\)**  
A palace slab panel has a concrete volume of 3 m³. Taking an illustrative unit weight of 25 kN/m³:  
\[
W=25\times3=75\text{ kN}
\]  
Meaning: its own weight contributes 75 kN before adding imposed loads and finishes.

### B. Beam and elastic section formulas

**B1. Simply supported beam under a central point load, \(M_{max}=PL/4\)**  
A simply supported demonstration beam has a 20 kN central load and a 4 m span.  
\[
M_{max}=20\times4/4=20\text{ kN·m}
\]  
Baahubali interpretation: the middle of the beam has the maximum sagging moment for this idealised load case.

**B2. Simply supported beam under UDL, \(M_{max}=wL^2/8\)**  
A beam spanning 5 m carries a uniform 4 kN/m load.  
\[
M_{max}=4\times5^2/8=12.5\text{ kN·m}
\]

**B3. UDL maximum support shear, \(V_{max}=wL/2\)**  
For the same beam:  
\[
V_{max}=4\times5/2=10\text{ kN}
\]  
Meaning: each support reaction is 10 kN in this symmetric case.

**B4. Cantilever with end point load, \(M_{support}=PL\)**  
A 3 kN hanging ornament is attached at the end of a 2 m cantilever.  
\[
M_{support}=3\times2=6\text{ kN·m}
\]  
Meaning: the fixed end must resist the largest bending moment.

**B5. Cantilever with full-length UDL, \(M_{support}=wL^2/2\)**  
A 2 m cantilever carries 2 kN/m uniformly.  
\[
M_{support}=2\times2^2/2=4\text{ kN·m}
\]

**B6. Rectangular second moment of area, \(I=bd^3/12\)**  
For a rectangular 200 mm wide and 300 mm deep beam section:  
\[
I=200\times300^3/12=450,000,000\text{ mm}^4
\]  
The depth is cubed, so increasing depth strongly increases bending stiffness.

**B7. Rectangular section modulus, \(Z=bd^2/6\)**  
For the same section:  
\[
Z=200\times300^2/6=3,000,000\text{ mm}^3
\]  
It is the bending-resistance indicator for that axis.

**B8. Elastic bending stress, \(\sigma=M/Z\)**  
If an illustrative bending moment is 30 kN·m and \(Z=3,000,000\text{ mm}^3\): convert moment to 30,000,000 N·mm.  
\[
\sigma=30,000,000/3,000,000=10\text{ N/mm}^2
\]  
Use this elastic formula only for the applicable elastic analysis; do not confuse it with the ultimate RCC stress block.

### C. Limit-state flexure of beams

**C1. Lever arm, \(z=d-0.42x_u\)**  
If effective depth \(d=450\) mm and neutral-axis depth \(x_u=150\) mm:  
\[
z=450-0.42(150)=387\text{ mm}
\]  
Baahubali interpretation: this is the distance between the compression resultant and the tension resultant in the idealised stress block.

**C2. Compression force, \(C=0.36f_{ck}b x_u\)**  
For illustration, use \(f_{ck}=25\) MPa, \(b=250\) mm, \(x_u=150\) mm:  
\[
C=0.36(25)(250)(150)=337,500\text{ N}
\]  
This force must be consistent with the tensile force in equilibrium.

**C3. Tension force in steel, \(T=0.87f_yA_{st}\)**  
For \(f_y=415\) MPa and \(A_{st}=1,000\) mm²:  
\[
T=0.87(415)(1000)=361,050\text{ N}
\]  
This particular example is not in equilibrium with C2; in a real design, solve for a compatible neutral axis or steel area rather than combining arbitrary values.

**C4. Moment resistance, \(M_u=0.36f_{ck}b x_u(d-0.42x_u)\)**  
For \(f_{ck}=25\) MPa, \(b=250\) mm, \(x_u=120\) mm, \(d=450\) mm:  
\[
M_u=0.36(25)(250)(120)(450-0.42(120))
\]
\[
M_u=270,000(399.6)=107,892,000\text{ N·mm}=107.9\text{ kN·m}
\]  
This is valid only when the assumed section, material grade and neutral axis meet code conditions.

**C5. Approximate tension steel from \(A_{st}\approx M_u/(0.87f_yz)\)**  
For an illustrative \(M_u=100\) kN·m, \(f_y=415\) MPa, \(z=400\) mm:  
\[
A_{st}\approx\frac{100\times10^6}{0.87(415)(400)}\approx692\text{ mm}^2
\]  
Then verify neutral axis, ductility, minimum/maximum reinforcement and detailing under IS 456.

**C6. Minimum beam steel, \(A_{st,min}=0.85bd/f_y\)**  
For \(b=250\) mm, \(d=450\) mm, \(f_y=415\) MPa:  
\[
A_{st,min}=0.85(250)(450)/415\approx230\text{ mm}^2
\]  
This is a minimum reinforcement check, not the complete flexural design.

**C7. Maximum beam tension steel, \(A_{st,max}=0.04bD\)**  
For \(b=250\) mm and overall depth \(D=500\) mm:  
\[
A_{st,max}=0.04(250)(500)=5,000\text{ mm}^2
\]  
The concrete must still be detailed and reinforced as required; this upper limit is not a target steel area.

### D. Shear and development length

**D1. Nominal shear stress, \(\tau_v=V_u/(bd)\)**  
For \(V_u=100\) kN, \(b=250\) mm and \(d=450\) mm:  
\[
\tau_v=100,000/(250\times450)=0.889\text{ N/mm}^2
\]  
Compare with the applicable code strength table and maximum shear stress limit.

**D2. Tension reinforcement percentage, \(p_t=100A_{st}/(bd)\)**  
For \(A_{st}=800\) mm², \(b=250\) mm, \(d=450\) mm:  
\[
p_t=100(800)/(250\times450)=0.711\%
\]  
Use this value with the applicable IS 456 shear-strength table.

**D3. Stirrups, \(V_{us}=0.87f_yA_{sv}d/s\)**  
Assume vertical stirrups with \(f_y=415\) MPa, total area of legs \(A_{sv}=157\) mm², effective depth \(d=450\) mm, spacing \(s=200\) mm:  
\[
V_{us}=0.87(415)(157)(450)/200\approx127,800\text{ N}=127.8\text{ kN}
\]  
Check the actual code limits, shear demand, stirrup spacing and maximum shear stress.

**D4. Development length, \(L_d=\phi\sigma_s/(4\tau_{bd})\)**  
Suppose a 16 mm bar has \(\sigma_s=0.87(415)=361.05\) MPa and an illustrative design bond stress of 1.92 MPa:  
\[
L_d=16(361.05)/(4(1.92))\approx752\text{ mm}
\]  
The bond stress must be selected from the correct code table with relevant bar type and concrete grade modifications. The numeric result is only an illustration.

### E. Slabs

**E1. One-way slab criterion**  
For a rectangular panel with spans 4 m and 8.5 m:  
\[
L_y/L_x=8.5/4=2.125>2
\]  
It generally acts one-way if the support conditions fit the rule. Baahubali analogy: the slab primarily spans across the shorter direction.

**E2. One-way simply supported moment, \(M=wL^2/8\)**  
For a one-metre strip with design load 8 kN/m and span 4 m:  
\[
M=8(4^2)/8=16\text{ kN·m per m strip}
\]  
Use effective span and the load basis required by the applicable design method.

**E3. Cantilever slab moment, \(M=wL^2/2\)**  
For a 1.5 m cantilever strip with \(w=6\) kN/m:  
\[
M=6(1.5^2)/2=6.75\text{ kN·m}
\]  
The top reinforcement near the support is important for the negative moment region.

**E4. Slab effective depth, \(d=D-\text{cover}-\phi/2\)**  
For overall thickness \(D=150\) mm, nominal cover 20 mm and main bar diameter 10 mm:  
\[
d=150-20-5=125\text{ mm}
\]  
For multiple layers, use the actual centroid of the tension reinforcement.

**E5. Minimum slab steel**  
For a 1 m wide strip, slab thickness 150 mm and high-strength deformed bars at 0.12%:  
\[
A_{s,min}=0.0012(1000)(150)=180\text{ mm}^2/\text{m}
\]  
Use the exact percentage and detailing limits required by the code and question.

### F. Columns

**F1. Simplified short tied-column capacity, \(P_u=0.4f_{ck}A_c+0.67f_yA_{sc}\)**  
For an illustrative case: \(f_{ck}=25\) MPa, \(A_c=90,000\) mm², \(f_y=415\) MPa and \(A_{sc}=1,000\) mm²:  
\[
P_u=0.4(25)(90,000)+0.67(415)(1,000)
\]
\[
P_u=900,000+278,050=1,178,050\text{ N}\approx1,178\text{ kN}
\]  
This expression applies only to the stated code case; check minimum eccentricity, slenderness and moment effects.

**F2. Steel percentage in a column, \(p=100A_{sc}/A_g\)**  
If steel area is 1,600 mm² and gross column area is 400,000 mm²:  
\[
p=100(1600)/400000=0.4\%
\]  
This is below the common 0.8% minimum in IS 456; the example therefore does not meet that usual minimum reinforcement condition.

**F3. Minimum eccentricity, \(e_{min}=l/500+D/30\), not less than 20 mm**  
Using illustrative unsupported length \(l=3000\) mm and dimension \(D=300\) mm:  
\[
e_{min}=3000/500+300/30=6+10=16\text{ mm}
\]  
Since this is less than 20 mm, the minimum eccentricity would be 20 mm. Use the exact code definitions of the relevant length and dimension.

**F4. Slenderness ratio, \(\lambda=l_e/D\)**  
If effective length is 3,000 mm and the corresponding dimension is 300 mm:  
\[
\lambda=3000/300=10
\]  
Check both axes and apply the relevant code's definition and classification criteria.

### G. Mix design

**G1. Water-cement ratio, \(w/c=W/C\)**  
If Baahubali's trial mix uses 180 kg water and 360 kg cement:  
\[
w/c=180/360=0.50
\]  
The chosen value must satisfy strength, workability and durability requirements; it is not chosen from strength alone.

**G2. Target mean strength, \(f'_{ck}=f_{ck}+1.65s\)**  
For M25 and standard deviation \(s=4\) MPa (illustrative):  
\[
f'_{ck}=25+1.65(4)=31.6\text{ MPa}
\]  
Use the standard deviation selection procedure in IS 10262 for the actual mix design.

**G3. Concrete volume and mass, \(m=\rho V\)**  
If an ingredient has a mass of 300 kg in a batch and occupies an absolute volume of 0.10 m³, then its implied density is \(300/0.10=3000\) kg/m³. In mix design, calculate each ingredient's absolute volume and ensure the batch yields the intended concrete volume.

### H. Working Stress Method (historical RCC theory)

**H1. Service stress check**  
If a hypothetical permissible compressive stress is 7 N/mm² and calculated service stress is 5.5 N/mm², then \(5.5<7\), so this particular check passes. Baahubali analogy: the service-load stresses stay below the chosen allowable limit.

**H2. Modular ratio, \(m=280/(3\sigma_{cbc})\)**  
If the historical permissible bending compressive stress \(\sigma_{cbc}=7\) N/mm²:  
\[
m=280/(3\times7)=13.33
\]  
Use only in the relevant historical WSM context, and verify the permitted concrete stress and code edition.

**H3. Transformed cracked-section neutral axis, \(bx^2/2=mA_{st}(d-x)\)**  
For a hypothetical beam with \(b=250\) mm, \(m=13.33\), \(A_{st}=800\) mm² and \(d=450\) mm, the equation becomes:  
\[
125x^2=10,664(450-x)
\]  
Expand and solve the quadratic for its positive physical root. This equation is an elastic cracked-section WSM model, not the limit-state neutral-axis formula.

## 17. Final exam strategy
When a formula appears, do these checks before calculating:
1. Identify the topic: flexure, shear, slab, column, bond, serviceability, mix design or WSM.
2. Identify the design method: service-load WSM or limit-state design.
3. Convert units before substitution.
4. Check whether the formula needs a table or coefficient.
5. Calculate, then check code limits and detailing requirements.
6. In MCQs, reject answers with incorrect units or inappropriate design assumptions first.
