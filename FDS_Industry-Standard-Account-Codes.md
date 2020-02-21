### Industry Standard Account Codes

contents:
* [Statement of Profit and Loss](#Statement-of-Profit-and-Loss).
  * [Revenue and/or Farm Trading](#Revenue-and/or-Farm-Trading).
  * [Other Revenue](#Other-Revenue).
  * [Farm Working Expenses](#Farm-Working-Expenses).
  * [Other Expenses](#Other-Expenses).
  * [Profit/Loss Calculations](#Profit/Loss-Calculations).
* [Balance Sheet](#Balance-Sheet).
  * [Equity](#Equity).
  * [Assets](#Assets).
  * [Liabilities](#Liabilities).
* [Source Accounts](#Source-Accounts).
  * [Beef Cattle Trading](#Beef-Cattle-Trading).
  * [Sheep Trading](#Sheep-Trading).
  * [Dairy Cattle Trading](#Dairy-Cattle-Trading).
  * [Milk Revenue](#Milk-Revenue).
  * [Wool Revenue](#Wool-Revenue).
  * [Other Farm Income](#Other-Farm-Income).
  * [Farm Operating Expenses](#Farm-Operating-Expenses).
  * [Repairs and Maintenance](#Repairs-and-Maintenance).
  * [Vehicles](#Vehicles).
  * [Rates and Insurance](#Rates-and-Insurance).
  * [Administration](#Administration).
  * [Interest, Rent and Lease](#Interest,-Rent-and-Lease).
  * [Other Income (Off Farm)](#Other-Income-(Off-Farm)).
  * [Other Expenses (Off Farm)](#Other-Expenses-(Off-Farm)).
  * [Depreciation, Amortisation and Sale of Plant, Property and Equipment](#Depreciation,-Amortisation-and-Sale-of-Plant,-Property-and-Equipment).
  * [Agricultural Produce on Hand](#Agricultural-Produce-on-Hand).
  * [Other Current Assets](#Other-Current-Assets).
  * [Property, Plant and Equipment](#Property,-Plant-and-Equipment).
  * [Investment in Shares](#Investment-in-Shares).

This part of the Appendix offers a standardised mapping system for a Farm Chart of Accounts. The Account Codes in this document are not intended to prescribe a reporting structure for financial reports, but rather to support mapping to a standardised coding for data interchange.

#### Statement of Profit and Loss

##### Revenue and/or Farm Trading

Mapping Code | Descriptor | Source Accounts
:----------- | :--------- | :--------------
1100 | Beef gross surplus/(deficit). | 3.1
1200 | Sheep gross surplus / (deficit). | 3.2
1300 | Dairy cattle gross surplus/(deficit). | 3.3
1400 | Total Milk revenue. | 3.4
1500 | Wool revenue. | 3.5
1600 | Cropping, Horticulture and Grazing revenue.
1700 | Lease income.
1900 | Other farm income. | 3.6
1000 | Total Farm Income. (Adjusted for Livestock Movement).

##### Other Revenue

Mapping Code | Descriptor | Source Accounts
:----------- | :--------- | :--------------
2000 | Other Income (Off Farm). | 3.13
2500 | Exceptional/capital revenue.	

##### Farm Working Expenses

Mapping Code | Descriptor | Source Accounts
:----------- | :--------- | :--------------
4100 | Farm Operating Expenses. | 3.7
4200 | Repairs and maintenance. | 3.8
4300 | Vehicles. | 3.9
4400 | Rates and insurance. | 3.10
4500 | Administration. | 3.11
4000 | Total Farm Working Expenses. |

##### Other Expenses

Mapping Code | Descriptor | Source Accounts
:----------- | :--------- | :--------------
5100 | Depreciation and Amortisation. | 3.15
5200 | Interest, rent and lease. | 3.12
5300 | Shareholders Remuneration / Drawings.	
5400 | Other Expenses (Off Farm). | 3.14
5500 | Income tax expense. | 
5600 | Exceptional/capital expenses.	|
 
##### Profit/Loss Calculations

A variety of profit and loss calculations are used across the industry. It is strongly recommended that organisations [SHOULD](docs/FDS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) pass only raw account data between systems, and implement profit and loss calculations after the data is received. If organisations choose to pass profit and loss calculations, they [MAY](docs/FDS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) use these codes to identify the data.

Mapping Code | Descriptor | Source Accounts
:----------- | :--------- | :--------------
6010 | Cash Operating Surplus.
6011 | Cash Operating Surplus – Discretionary Cash.
6012 | Cash Operating Surplus/Deficit.
6020 | Earnings before Interest Tax Depreciation Amortisation and Rent (EBITDAR).
6025 | Earnings before Interest Tax and Rent (EBITR).
6030 | Dairy Operating Profit.
6031 | Dairy Operating Profit – Business Profit before Tax.
6032 | Dairy Operating Profit – Equity Growth from Profit.
6040 | Net Farm Surplus/(Deficit).
6045 | Total Operating Profit.
6050 | Surplus/(Deficit) after Shareholders Remuneration.
6060 | Net Profit/(Loss) before Tax.
6070 | Net Profit/(Loss) after Tax.
 
#### Balance Sheet

These mapping codes [MAY](docs/FDS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) be used in developing messages for interchange of actual financial statements for benchmarking and analysis.

##### Equity
Mapping Code | Descriptor 
:----------- | :--------- 
9100 | Issued capital.
9210 | Retained earnings/(Accumulated losses) – Opening Balance.
6070 | Retained earnings/(Accumulated losses) - Net profit/(loss) after Tax.
9220 | Retained earnings/(Accumulated losses) - Dividend paid to owners.
9200 | Retained earnings/(Accumulated losses) - Closing balance.
9310 | Livestock Revaluation Reserve - Opening balance.
9320 | Livestock Revaluation Reserve - Holding gains/(losses) on revaluation of livestock.
9330 | Livestock Revaluation Reserve - Transfer to retained earnings on disposal of livestock.
9300 | Livestock Revaluation Reserve - Closing balance.
9410 | Asset Revaluation Reserve - Opening balance.
9420 | Asset Revaluation Reserve - Revaluation of land and buildings.
9430 | Asset Revaluation Reserve - Revaluation of investment shares.
9400 | Asset Revaluation Reserve - Closing balance.
9510 | Realised Capital Reserve -Opening balance.
9520 | Realised Capital gain(loss) on sale.
9500 | Realised Capital Reserve - Closing balance.
9000 | Total - Equity.
 
##### Assets

Mapping Code | Descriptor | Source Accounts
:----------- | :--------- | :--------------
7110 | Bank and short-term deposits 	
7120 | Account receivables 	
7130 | [GST](docs/FDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) Receivable.
7140 | Income equalisation deposit.
7150 | Agricultural produce on hand. | 3.16
7160 | Income tax receivable. 	
7170 | Other current assets. | 3.17
7100 | Total - Current Assets. 	
7200 | Property, plant and equipment. | 3.18
7300 | Investment property. 	
7400 | Livestock on hand. | 3.1, 3.2, 3.3
7500 | Investment in shares. | 3.19
7600 | Term deposits.	
7700 | Other non-current assets.	
7800 | Related party loans.
7900 | Total - Non-Current Asset.
7000 | Total - Assets.
7999 | Net  Assets.

##### Liabilities

Mapping Code | Descriptor 
:----------- | :--------- 
8110 | Bank overdrafts.
8120 | [GST](docs/FDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) payable.
8130 | Income tax payable.
8140 | Account payables.
8150 | Current portion term loans.
8160 | Current portion finance leases & hire purchases.
8100 | Total - Current Liabilities.
8200 | Non-current loans.
8300 | Non-current finance leases & hire purchases.
8400 | Other non-current liabilities.
8500 | Related Parties Loan Accounts.
8600 | Shareholder advance accounts.
8700 | Family loans.
8800 | Total - Non-Current Liabilities.
8000 | Total - Liabilities.

#### Source Accounts 

These mapping codes [MAY](docs/FDS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) be used in developing messages for interchange of actual financial statements for benchmarking and analysis.

##### Beef Cattle Trading

Mapping Code | Descriptor 
:----------- | :--------- 
1111 | Sales - Beef Rising I year heifers.
1112 | Sales - Beef Rising 2 year heifers.
1113 | Sales - Beef Rising 3 year heifers.
1115 | Sales - Beef Mixed Age cows. 
1116 | Sales - Beef Rising 1 year steers/bulls. 
1117 | Sales - Beef Rising 2 year steers/bulls. 
1118 | Sales - Beef Rising 3 year steers/bulls.
1120 | Sales - Beef Mixed Age steers/bulls.
1121 | Sales - Beef Rising I year Breeding bulls.
1122 | Sales - Beef Rising 2 year Breeding bulls.
1123 | Sales - Beef Rising 3 year Breeding bulls.
1125 | Sales - Beef Mixed Age Breeding bulls.
1110 | Total Sales - Beef Cattle.
1131 | Purchases - Beef Rising I year heifers. 
1132 | Purchases - Beef Rising 2 year heifers.
1133 | Purchases - Beef Rising 3 year heifers.
1135 | Purchases - Beef Mixed Age cows. 
1136 | Purchases - Beef Rising 1 year steers/bulls. 
1137 | Purchases - Beef Rising 2 year steers/bulls. 
1138 | Purchases - Beef Rising 3 year steers/bulls.
1140 | Purchases - Beef Mixed Age steers/bulls.
1141 | Purchases - Beef Rising I year Breeding bulls.
1142 | Purchases - Beef Rising 2 year Breeding bulls.
1143 | Purchases - Beef Rising 3 year Breeding bulls.
1145 | Purchases - Beef Mixed Age Breeding bulls.
1130 | Total Purchases - Beef Cattle.
1181 | Beef Cattle Cash Trading Surplus.
1182 | Beef Cattle Deaths and missing. 
1183 | Beef Cattle Natural increase.
1184 | Beef Cattle (Trading) Effect of change in numbers. 
1100 | Beef Cattle Gross surplus/(deficit). 
7411 | Market Value - Beef Rising I year heifers. 
7412 | Market Value - Beef Rising 2 year heifers.
7413 | Market Value - Beef Rising 3 year heifers.
7415 | Market Value - Beef Mixed Age cows. 
7416 | Market Value - Beef Rising 1 year steers/bulls. 
7417 | Market Value - Beef Rising 2 year steers/bulls.
7418 | Market Value - Beef Rising 3 year steers/bulls.
7420 | Market Value - Beef Mixed Age steers/bulls.
7421 | Market Value - Beef Rising I year Breeding bulls.
7422 | Market Value - Beef Rising 2 year Breeding bulls.
7423 | Market Value - Beef Rising 3 year Breeding bulls.
7425 | Market Value - Beef Mixed Age Breeding bulls.
7410 | Total Market Value - Beef Cattle on Hand.  
1190 | Market Value - Beef Cattle Holding Gains/(Loss). 
1195 | Market Value - Beef Cattle Effect of change in numbers.
 
##### Sheep Trading

Mapping Code | Descriptor 
:----------- | :--------- 
1211 | Sales - Ewe Lambs.
1212 | Sales - Ram Lambs.
1213 | Sales - Wether Lambs.
1215 | Sales - Lambs.
1216 | Sales - Ewe Hoggets.
1217 | Sales - Ram Hoggets.
1218 | Sales - Wether Hoggets
1219 | Sales - Breeding Ram Hoggets.
1220 | Sales - Hoggets. 
1221 | Sales - Two-tooth Ewes.
1222 | Sales - Four-tooth Ewes.
1225 | Sales - Mixed Age Ewes.
1226 | Sales - Two-tooth Rams.
1227 | Sales - Four-tooth Rams.
1230 | Sales - Mixed Age Rams.
1231 | Sales - Two-tooth Wethers.
1232 | Sales - Four-tooth Wethers.
1235 | Sales - Mixed Age Wethers.
1240 | Sales - Mixed Age Breeding Rams.
1210 | Total Sales - Sheep.
1251 | Purchases  - Ewe Lambs.
1252 | Purchases  - Ram Lambs.
1253 | Purchases  - Wether Lambs.
1255 | Purchases  - Lambs 
1256 | Purchases  - Ewe Hoggets.
1257 | Purchases  - Ram Hoggets.
1258 | Purchases  - Wether Hoggets.
1259 | Purchases  - Breeding Ram Hoggets.
1260 | Purchases  - Hoggets.
1261 | Purchases  - Two-tooth Ewes.
1262 | Purchases  - Four-tooth Ewes.
1265 | Purchases  - Mixed Age Ewes.
1266 | Purchases  - Two-tooth Rams.
1267 | Purchases  - Four-tooth Rams.
1270 | Purchases  - Mixed Age Rams.
1271 | Purchases  - Two-tooth Wethers.
1272 | Purchases  - Four-tooth Wethers.
1275 | Purchases  - Mixed Age Wethers.
1280 | Purchases  - Mixed Age Breeding Rams.
1230 | Total Purchases - Sheep.
1281 | Sheep - Cash trading surplus.
1282 | Sheep - Deaths and missing.
1283 | Sheep - Natural increase. 
1284 | Sheep Trading - Effect of change in numbers. 
1200 | Sheep Trading - Gross surplus/(deficit).
7431 | Market Value - Ewe Lambs.
7432 | Market Value - Ram Lambs.
7433 | Market Value - Wether Lambs.
7435 | Market Value - Lambs. 
7436 | Market Value - Ewe Hoggets.
7437 | Market Value - Ram Hoggets.
7438 | Market Value - Wether Hoggets.
7439 | Market Value - Breeding Ram Hoggets.
7440 | Market Value - Hoggets.
7441 | Market Value - Two-tooth Ewes.
7442 | Market Value - Four-tooth Ewes.
7445 | Market Value - Mixed Age Ewes.
7446 | Market Value - Two-tooth Rams.
7447 | Market Value - Four-tooth Rams.
7450 | Market Value - Mixed Age Rams.
7451 | Market Value - Two-tooth Wethers.
7452 | Market Value - Four-tooth Wethers.
7455 | Market Value - Mixed Age Wethers.
7456 | Market Value - Mixed Age Breeding Rams.
7430 | Total Market Value - Sheep on Hand. 
1290 | Market Value Sheep - Holding Gains/(Loss).
1295 | Market Value Sheep - Effect of change in numbers.
 
##### Dairy Cattle Trading

Mapping Code | Descriptor 
:----------- | :--------- 
1315 | Sales - Bobby Calves.
1316 | Sales - Dairy Calves.
1321 | Sales - Dairy Rising 1 year heifers. 
1322 | Sales - Dairy Rising 2 year heifers. 
1323 | Sales - Dairy Rising 3 year heifers.
1325 | Sales - Dairy Mixed age cows. 
1326 | Sales - Dairy Rising 1 year steers/bulls. 
1327 | Sales - Dairy Rising 2 year steers/bulls. 
1328 | Sales - Dairy Rising 3 year steers/bulls.
1330 | Sales - Dairy Mixed Age steers/bulls.
1335 | Sales - Dairy Breeding bulls. 
1310 | Total Sales - Dairy Cattle.
1351 | Purchases - Dairy Calves. 
1352 | Purchases - Dairy Rising 1 year heifers. 
1353 | Purchases - Dairy Rising 2 year heifers. 
1354 | Purchases - Dairy Rising 3 year heifers.
1355 | Purchases - Dairy Mixed age cows. 
1356 | Purchases - Dairy Rising 1 year steers/bulls. 
1357 | Purchases - Dairy Rising 2 year steers/bulls. 
1358 | Purchases - Dairy Rising 3 year steers/bulls.
1360 | Purchases - Dairy Mixed Age steers/bulls.
1365 | Purchases - Dairy Breeding bulls. 
1350 | Total Purchases - Dairy Cattle.
1381 | Dairy Cattle Cash trading surplus. 
1382 | Dairy Cattle Deaths and missing.
1383 | Dairy Cattle Natural increase. 
1384 | Dairy Cattle (Trading) Effect of change in numbers. 
1300 | Dairy Cattle Gross surplus/(deficit).
7471 | Market Value - Dairy Rising 1 year heifers.
7472 | Market Value - Dairy Rising 2 year heifers. 
7473 | Market Value - Dairy Rising 3 year heifers.
7475 | Market Value - Dairy Mixed age cows. 
7476 | Market Value - Dairy Rising 1 year steers/bulls. 
7477 | Market Value - Dairy Rising 2 year steers/bulls. 
7478 | Market Value - Dairy Rising 3 year steers/bulls.
7480 | Market Value - Dairy Mixed Age steers/bulls.
7485 | Market Value - Dairy Breeding bulls. 
7470 | Total Market Value - Dairy Cattle on Hand. 
1390 | Market Value Dairy Cattle - Holding Gains/(Loss).
1395 | Market Value Dairy Cattle - Effect of change in numbers.
 
##### Milk Revenue

Mapping Code | Descriptor 
:----------- | :--------- 
1401 | June
1402 | July
1403 | August
1404 | September
1405 | October 
1406 | November
1407 | December 
1408 | January 
1409 | February 
1410 | March 
1411 | April
1412 | May 
1413 | Capacity adjustment.
1430 | Total Milk Revenue - Deferred.
1431 | Total Milk Revenue - Advanced.
1440 | Other Milk Income.
1450 | Milk Production Insurance.
1460 | Payments to Sharemilkers and Contract Milkers.
1400 | Total Milk Revenue.
1498 | Average milk income/kg.
1499 | Milk Solids Last Season.

##### Wool Revenue

Mapping Code | Descriptor 
:----------- | :--------- 
1510 | Wool sales.
1520 | Crutchings and dags. 
1530 | Total wool sales and crutchings/dags.
7151 | Opening wool on hand. 
7152 | Closing wool on hand.
1500 | Total Wool Revenue and Production.
1590 | Average Net Price per kilo.
 
##### Other Farm Income

Mapping Code | Descriptor 
:----------- | :--------- 
1910 | Milk Co / Processor Dividends.
1920 | Rebates 
1930 | Rental, lease and licence income.
1940 | Timber sales.
1950 | Sale of forestry carbon credits.
1960 | Expenditure carried forward.
1970 | Sundry 
1900 | Total - Other Farm Income.

##### Farm Operating Expenses

Mapping Code | Descriptor 
:----------- | :--------- 
4101 | Animal health. 
4102 | Breeding.
4103 | Calf rearing 
4104 | Dairy shed expenses. 
4105 | Deferred Expenditure.
4106 | Dog and horse. 
4107 | Electricity and gas (excluding private use). 
4108 | Fertiliser
4109 | Freight and cartage. 
4110 | General expenses. 
4111 | Grazing 
4112 | Horticulture Operating Expenses.
4113 | Industry Levies.
4114 | Irrigation
4115 | Pasture renovation. 
4116 | Protective clothing.
4117 | Shearing wages.
4118 | Shearing expenses. 
4119 | Staff training.
4120 | Stock feed grown/made.
4121 | Stock feed purchased.
4122 |Wages and salaries. 
4123 | Weed and pest. 
4100 | Total - Farm Operating Expenses.

##### Repairs and Maintenance

Mapping Code | Descriptor 
:----------- | :--------- 
4210 | Buildings 
4215 | Dwelling 
4220 | Fences and yards. 
4225 | General repairs. 
4230 | Plant and machinery. 
4235 | Tools and hardware.
4240 | Drains, races tracks and bridges. 
4245 | Water supply. 
4250 | Effluent disposal. 
4255 | Hedges and shelters. 
4200 | Total - Repairs and Maintenance.

##### Vehicles

Mapping Code | Descriptor 
:----------- | :--------- 
4310 | Farm vehicle. 
4320 | Fuel and oil. 
4330 | Tractor 
4300 | Total - Vehicle.

##### Rates and Insurance

Mapping Code | Descriptor 
:----------- | :--------- 
4410 | ACC levies. 
4420 | Insurance 
4430 | Rates 
4400 | Total - Rates and Insurance.
 
##### Administration

Mapping Code | Descriptor 
:----------- | :--------- 
4505 | Administration 
4510 | Accountancy fees. 
4515 | Bank fees. 
4520 | Computer 
4525 | Entertainment 
4530 | Farm advisory fees. 
4535 | Fringe benefit tax. 
4540 | General administration. 
4545 | Governance
4550 | Legal 
4555 | Professional and consulting fees. 
4560 | Professional Development and Training.
4565 | Resource Consents and Compliance.
4570 | Seminars 
4575 | Subscriptions 
4580 | Telecommunications 
4585 | Travel and accommodation. 
4500 | Total - Administration.

##### Interest, Rent and Lease

Mapping Code | Descriptor 
:----------- | :--------- 
5210 | Interest - overdraft. 
5215 | Interest - term loans. 
5220 | Interest - hire purchase. 
5225 | Interest - related parties. 
5230 | Interest - finance lease. 
5235 | Land lease. 
5240 | Land lease - related parties. 
5245 | Operating lease. 
5200 | Total - Interest Rent and Leases.
 
##### Other Income (Off Farm)

Mapping Code | Descriptor 
:----------- | :--------- 
2010 | Salary, Wages Fees Received.
2015 | Interest Received.
2020 | Dividends
2025 | Rent/Lease Received.
2030 | ACC/Insurance Protection Income.
2035 | Contracting >$10,000.
2040 | Machinery Hire.
2045 | Business
2050 | Foreign exchange gains / (loss).
2055 | FBT personal contributions.
2060 | Fonterra Distributions.
2065 | Other / Sundry.
2000 | Total - Other Income (Off Farm).

##### Other Expenses (Off Farm)

Mapping Code | Descriptor 
:----------- | :--------- 
5410 | Rental Expenses.
5415 | Business Expenses.
5420 | Contracting Expenses.
5425 | Other
5400 | Total - Other Expenses (Off Farm).

##### Depreciation, Amortisation and Sale of Plant, Property and Equipment

Mapping Code | Descriptor 
:----------- | :--------- 
5110 | Depreciation 
5120 | Development expenditure amortisation.
5130 | Loss/(Gain) on sale of Plant, Property and Equipment.
5100 | Total - Depreciation and Amortisation.
 
##### Agricultural Produce on Hand

Mapping Code | Descriptor 
:----------- | :--------- 
7152 | Wool
7153 | Stock Feed on Hand.
7154 | Harvested Crops.
7155 | Other inventory.
7150 | Total - Agricultural Produce on Hand.

##### Other Current Assets

Mapping Code | Descriptor 
:----------- | :--------- 
7171 | Property, Plant and Equipment under construction.
7172 | Prepayments and Deferred Expenditure.
7173 | Deposit on farm.
7174 | Deposit on livestock.
7175 | Rental Bond.
7100 | Total - Other Current Assets.

##### Property, Plant and Equipment

Mapping Code | Descriptor 
:----------- | :--------- 
7210 | Land (including Capital Development and Improvements).
7220 | Buildings
7230 | Plant and Machinery.
7240 | Leasehold Improvements.
7250 | Motor Vehicles.
7260 | Fixtures, fittings and equipment.
7200 | Total - Property, Plant and Equipment.
 
##### Investment in Shares

Mapping Code | Descriptor 
:----------- | :--------- 
7510 | Dairy Company Shares.
7520 | Meat Company Shares.
7530 | Fertiliser Company Shares.
7540 | Other Farming Shares.
7550 | Off Farm Shares.
7560 | Off Farm and Other Investments.
7500 | Total - Investment in Shares.
