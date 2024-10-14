# assignment-4
# Experimental Determinations

Gca = float(input ("Enter the value of specific gravity of CA: ")
Gfa = float(input("Enter the value of specific gravity of FA: ")
Gc = float(input("Enter the value of specific gravity of Cement: "))
Water_Density = float(input("Enter the value of Water Density: ")
AGG Size = float(input('" Enter the nominal Size of Aggregate: "))
Nature of _AGG = input("Nature of Aggregates:")
Slump = float(input('"Enter the value of workability of concrete: ")
Admixture = input("Type of Admixture:")
Exposure_Condition = input("Exposure Condition:")
Concreting = input("Type of Concreting:")
Zone = int(input("Zone: ")

# Target Mean Strength

sigma = {
10:3.5,
15:3.5,s
20: 4,
25:4,
30: 5,
35: 5,
40: 5,
45: 5,
50: 5,
55: 5

74

ft = fck + sigma[fck]*1.65
print ("Target Mean Strength: ", ft, "MPa'")

# Maximum free Water Cement Ratio
# Reference IS 456: 2000 Table 5

if(Concreting == "Plain"):
WC_ratio = {

}
else:
"Mild" : 0.6,
"Moderate" :0.6,
"Severe" :0.5,
"Very Severe" :0.45,
"Extreme":0.4

WC_ratio ={
"Mild": 0.55,
"Moderate":0.5,
"Severe" :0.45,
"Very Severe" :0.45,
"Extreme":0.4

print ("W/C Ratio:", WC_ratio[Exposure_Condition] )
WC_ratio = WC_ratio [Exposure_Condition]

# Minimum Cement Content

if(Concreting == "plain"):
Min_Cement_Content = {

else:
"Mild":220,
"Moderate": 240,
"Severe": 250,
"Very Severe": 260,
"Extreme": 280

Min_Cement_Content = {
"Mild": 300,
"Moderate" :300
"'Severe'": 320,
"Very Severe" :340,
"Extreme": 360

print ("Minmum Cement Content:", Min_Cement_Content[Exposure_Condition], "kg/m^3")

# Water Content

Water
10:208,
20:186,
40:165

Water_Content = Water_Content[AGG_Size]
if (Slump == 75):
Water_Content = Water_Content + Water_Content*0.03
elif (Slump == 100):
Water Content = Water Content + Water Content*0.06
elif (Slump == 125):
Water Content = Water

76

Content = {

Content+ Water Content*0.09

elif (Slump == 150):
Water_Content = Water_Content + Water Content*0.12
elif (Slump == 175):
Water Content = Water Content + Water Content*0.15
elif (Slump == 200):
Water Content = Water

if (Nature_of_AGG == 'Sub-Angular"):
Water
elif (Nature_of_AGG == "Gravel"):
Water_Content = Water_Content - 20
elif (Nature_of_AGG == "Round"):
Water_Content = Water

if (Admixture == "Plastisizer"):
Water_Content = VWater_Content-(0.1*Water Content)
elif (Admixture=="Super-plastisizer"):
Water Content = Water Content-(0.2 *Water Content)

print ("Water Content: ", Water_Content, "kg/m^3")

# Cement Content

Cement Content = Water Content/WC ratio
print ("Cement Content:", Cement Content, "kg/m^3")

print ("As Per IS 456:2000, Maximum allowed Cement Content is 450 kg/m^3")

if (Cement_Content< 450):

else:
Cement_Content = Cement Content

77

Content+ Water Content*0.18

Content = Water Content - 10

Content -25

Cement_Content = 450

if Cement Content< 450:
print ("Safe")

# Volume Calculations

Vol_Cement = Cement_Content/(Gc*Water_Density)
print ("Volume of Cemnet: ", Vol_ Cement, "m^3")

Vol_Water = Water_Content/Water_Density
print ("Volume of Water: ", Vol_Water, "m^3")

Vol AGG= 1-Vol Water-Vol_Cement
print ("Volume of Course Aggregates and Fine Aggregates: ", Vol_AGG, "m^3")

Zone ID =}
Zone_ID[1]= {10:0.44, 20:0.60, 40:0.69}

Zone_|D[2]={10:0.46, 20:0.62, 40:0.71}

Zone ID[3]={10:0.48, 20:0.64, 40:0.73}

Zone_iD[4]={10:0.5, 20:0.66, 40:0.75)

Fraction = Zone_ID[Zone] [AGG_Size]

if (WC_ratio==0.5) :
Fraction=Fraction
elif (WC_ ratio==0.45):
Fraction=Fraction+(0.01*Fraction)

78

elif (WC_ratio==0.4):
Fraction=Fraction+(0.02 * Fraction)
elif (WC_ratio==0.55):
Fraction=Fraction-(0.01*Fraction)
elif (WC_ratio==0.60):
Fraction=Fraction-(0.02*Fraction)

print ("Course Aggregate fraction:", Fraction)

Vol_CA = Vol_AGG*Fraction
print ("Volume of Course Aggregate:", Vol_CA,"m^3")

Vol_FA = Vol_AGG-Vol_CA
print ("Volume of Fine Aggregate: ", Vol_FA,"m^3")

Mass_CA= Vol_CA*Gca* Water_Density
print ("Mass of Course Aggregates: ", Mass_CA, "Kg/m^3")

Mass_FA = Vol_FA*Gfa*Water_Density
print ("Mass of Fine Aggregates:", Mass_FA, "kg/m^3")

# Ratios
print ("Weight Batching")
print
(Cement_Content/Cement_Content,"", Mass_FA/Cement_Content,":", Mass_CA/Cement_Content,":
",Water_Content/Cement_Content)

print ("Volume Batching:")
print

79

(Vol_Cement/Vol_Cement,"", Vol_FA/Vol_Cement,"", Vol_CAWol_Cement,"" Vol_Water/Vol_Ceme
nt)
