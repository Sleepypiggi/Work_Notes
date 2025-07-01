Prophet Array is a loop
Where each iteration of the loop is stored in an array index

Prophet is smart enough to optimise the calculations to know which variable have dependencies needs to be calculated first
They should give you training. Understand structures, structure links and dynamic processing and you will be ahead of the game. The Example Model Office is a great learning tool.

Prophet

Whether a product is run as new business or in force is controlled by 

LAST SPCODE FOR EXISTING BUSINESS > Inside run structure

Some codings may change based on this, don’t mix up

Either change MPFILE or SPCODE

Decrement Order >
Lapse is always last because intuitive, you already paid for the current year of coverage. Will stay on till the next payment then skip
FOLLOWS PREMIUM FREQUENCYY

Prophet is about controls and governance that’s why it’s popular
Prophet Parameter vs Read Parameter
Maybe different runs you don’t want that parameter, so can disable if use formula
Prophet is a series of functions that is combined into a product
Before Val date use actual, future use beer

Balance sheet variable not summed, shows as at the latest date

P&L variable summed if extracting over a range of dates (EG Y1)

Public Variable >> What they want to read out

Private variable >> Foe the extended formula only

Prophet can be cleaned up

A lot of common coding can be streamlined into reusable indicators 

EG = IF within projection period etc then 1, if RBC2 then 1


Main advantage of prophet is master product, same as


Prophet ! Is used to denote the first row


RI expect an inflow because Recovery got PAD, but premium no PAD

Assuming same underlying risk


Read table of tables need to use read generic table text

Proficiency in Prophet including advanced features like extended formulas, calculation looping, rebasing, modules, ALS is desirable
Prophet different definitions

# **Prophet**

## Overview

Prophet is a propietary software used to "model" insurance products
 Takes In a set of assumptions, parameters and product features and generates the cashflows for that product
cashflows can be manipulated to calculate other things like EV etc

Why Prophet?
 can be easily done In excel, why need to use this propietary software?
-- Ensure that everyone is using the same set of assumptions/excel; excel may have some error
 Built In product features?

## Key Components

Library
 Collection of commonly used variables
 Conventional Library (for non ULP) & Unit Linked Library (for ULP)
-- Note that a variable is not just a name; it is a name which contains a definition
-- Different types of Variables:
-- Formula (F), transformation of other variables
-- Global (G), value taken from Global table
-- Parameter (P), value taken from Parameter table
-- Model Point (M), value taken from Model Point

Products
-- The "model" which connects the various variables together to generate the cashflows
-- Models built from the conventional library start with "C" while those from the Unit library start with "U"
 There are fundamentally only a few types of products (non Par Insurance, Par Insurance, ILP, non Par Annuity, Par Annuity)
 products sold In the market are simply variations of these products with a subset of the features or based on different assumptions
 Master products are used to Model the common features of these products
 Individual Specific products are Built off these Master products, known as same as products
 They inherit (In a programming sense) the features of these Master products > no need to spend time coding the same features again for each product
 If There are any changes made to these shared features In the Master product, They will automatically flow through the same as products  > no need to spend time to individually change every product
 can control which features that each same as product inherits from the Master product using Flag variables

Tables
 Tables contain the assumptions used In the modelling process
 Global table: assumptions that are fixed In value & apply to all products (Run Number X variable name)
 Parameter table: fixed In value & apply to Individual products (variable name X product)
-- Mainly used to control which product features inherited from the Master Model & other high level assumptions
-- Thus, seperated based on Conventional & Unit Linked
-- Generic Tables: 
 Tables of Tables: Tables

 Generic table: Depend on other variables to determine their values

Run Setting
 control metadata about the Run
 Run Specific paramaters: Valuation Date, Type of output etc
-- Table path locations:
---- Multiple paths can be listed for each table; prophet will search the first path for the tables before the second path
-- Hierarchical structure of reading Tables

Run Structure
 States which products to Run and how to group them together
 Some system level definitions are provided here as well, as well as Some metadata

Job (PE Specific) > Putting everything together, select values for the variables here


Summary Library

Level Number > Sequence of calculation
Priorrity system > level 1 is faster

200 > New businessSPCODE
below 200 > IF

Prophet > last sp code for existing business > Means only applies for new business

Keeps everything on memory then outputs

Domain > Everyone
Workspace within domain as many


Workers > Core groups

Upload workspace

Prophet Extration
Proj_Result extracts the numbers from the prophet result file
Sometimes results in error cos product cannot be fond etc
N() to coerce the errors into 0 so that can still sum

Problem is that when extracting a lot of variables at a time, can sometimes crash then get everything erorr or 0
Not sure whether truly 0 or error
Need to slowly recurse

101
102
103
141



Summary Run > Accumulate cashflows into one model point, easier to read

Edits made into Library, compare library to get up to date
Master product contains everything, same as products then control which features to have via flags

SPCODE = Sub Product Code
1 = Jan, 12 = Dec
0 = Whole year

PE Lost contact with worker -- Global/Param Tables have issues
PE if got duplicate, will name _1 in the P drive
Post prod workspace is locked at one machine per run to avoid cannibalising resources from Prod

PROPHET
Tabs at the side or side
MPF will reas relative

Base is where the workspace is open
Run Structure > Product & Accumulation
Run setting > Table locations, table hierarchy
Always validate run settings to check if the path exists

Future Accumulation > Projection length
Past accumulation > Duration if, if u want to see those periods

103 > IF
141 > NB

Unit test > Run the first model point

Two different result foiles
 PROJ File > Call from excel, all years, newbus File, same location as RPT
 RPT > Individual Model Point result File, only Valuation Date
 PROJ tends to be bigger
 Controlled variable group
 If you Call PP variable for PROJ, it will only show first MPT

Can run on multiple machines, but the machines must be able to write to those paths
BPA345

Levels > Priority level
Lower level run first
Product level 10
Summary 11 > Conversion to USD
Accumulation 15/16
Summary 25

Must add new products into accumulation/structure
Prophet Master Model will tell u where to put > Flow chart
Check against the spreadsheet

Table Editor
Dont open in prophet because take prophet license

No more space in text

SPCode is a unique identifier, up to u to define
Within NBEV output, it represents the month that the policy is incepted

Indicator
Different version of the same formula
Can also be used to select indicators

Projection view > Results diagram view > Shows the variable

IF and NB MPF file is different

Differentiate SPCODE in MPF to call out individual results
Run only first model point > Groups by SPCODE
Runs every first SPCODE

If got RI > Defined based RCH Code. Defined by

Table name > Controls all the tables

NB CODING 2

Extended Formula
Custom Formula, not provided by FIS
Think of it like an object
that can output other variables

Can have super model but split for efficiency
Result Diagram View > Need result

Master product > Product Diagram View > Spiderweb
Variable > Click around
FLAG SYSTEM = Control whether the benefit is used



Press validate to check if tables exist

Rong Kang Can approve if
 non year end
 no assumption change
 change In methodology
 Threshold

Model must be ready by 1st of the month
1 week review & fix time
Send early
Run whole in force even for early check

Compare Library > OUTPUTS text file > Macro in excel to pick up the changes

1. Run Structure -- tells Prophet which products to run. How come when run single product still need
2. Flag Mapping -- How do I know what the values mean for each flag? Not everything is 1/0 (Check Variable Properties)
3. Highlighted words -- Blue is keyword, green is numbers, black is variables, red is prophet defined function/variable (Can search inside the helper function)

Variable Groups > Control which variables are output
Model Point File edit > Workspace can edit, full proof like excel

If only want to run 1-2 model point, select all (CTRL A) then exclude all
find the model point u want, include that row only
This can be controlled in the formatting file by excluding * (to confirm)

PROJ function > Reads from result file
rpt file > INDIVIDUAL model point
Should reconcile with each other

Change prophet output format
 Number
 time period, set monthly


If got MPF change, need to ask RBC2 team to regenerate latest month & YE MPF based on the new structure
Becos some source system got no monthly snapshot, they need to patch

Import Variable > Insert or replace
Backup old workspace into PUBZ

Portfolio Impact Checking
 Compares all key variables from previous Model and current Model based on last month end position
-- Rerun BOTH positions (Including last month end; dont just take the production run)
 File will extract results for all variables at product level and compare them
 Check that opening position is correct
 Check the impact to key variables at the fund level
 Check to see If They are expected

Run Setting
Controls everything
Set valuation Date
choose output type > Sup product or just total, can save space
Choose RPT file & variables to output for each (can be different)

if you wanna test, can run with 1st MPT for each spcode first
Good to test MPF first then run the full thing

In Force SP Code = 100 - 199
New Business SP Code = 200+
LAST_SPCODE_FOR_EXISTING_BUS = 199

Therefore SP_CODE > LAST_SPCODE -> New business only

Deaths assume to occur middle of month - 
    LAPSE_TMING = 1 means Lapse EOM; die first then remaining ppl lapse
    LAPSE_TMING = 0.5 means Lapse middle OM; compete with deaths

pp run first model point of each SP CODE by defualt, need to change accordingly

Decrement Rate modelling is very important
The base decrement may be ok, but model is always subject to various shocks
Rate should be floored at 0 or capped at 1
Test robustness by shocking an insane amount (EG. 500% or something)

Coding Tips
1. Maintain consistency across products
2. Make your code readable by using "_" to add a new line, similar to VBA
3. Minimize reading tables. If it is a constant, read once at inception (t=0) then all other time periods refer back to that period. If read quarterly or yearly, same concept -> Read only at that time period then refer back. Reason is because reading is an expensive process computationally, thus avoid looking up too much.
4. If a variable varies by time, add (t) behind the variable to denote it. This makes it more readable
5. You can refer to the variable name as a string using VAR_NAME


Prophet table formatting - Consistent number of DPs
Hard to see in excel, open in notepad/propview

Build things to be modular, but if there is no way to test it then dont build it
You cannot ensure that it will be correct, no way to test it.



Time dependent
Reading time-dependent generic tables in Prophet programming language
If a generic table is accessed for each month of the projection it can have a significant impact on performance because of the number of times the table needs to be searched. You should therefore try to limit your use of time-dependent generic tables where possible and you should also try to access them annually rather than monthly.

If you use the READ_GENERIC_TABLE function you should use If Then Else statements to reduce the number of times the generic table is read to the minimum. For example, the following formula might be used for UFII_PC so that the generic table is read annually instead of monthly:

IF t=0 THEN
0
ELSE IF mult(t-1,12) THEN
READ_GENERIC_TABLE("TABNAME","Y","VAR_NAME",CALENDAR_YR)
ELSE

UFII_PC(t-1)

Within Prophet a product is a collection of variables that together represent the desired calculations.

A simple product without Rebasing
Within Prophet a product is a collection of variables that together represent the desired calculations. Each variable can be defined in a number of ways – constants, tables, formulas, extended formulas, etc. The definition of a particular variable can reference another variable.

When a run is carried out, Prophet analyses all the variables in a product. It determines all the appropriate dependencies between the variables and then organises the variables into building blocks. Together these building blocks form a complete representation of the actuarial model defined individually in each of the variables.

Typically a product will contain some variables that have a constant value for all time and others that change with time. Prophet is designed to organise the variables that depend on time into an efficient sequence. Some variables are calculated in an ascending time order, while others are calculated in a descending time order. Some variables will be grouped together so that they are calculated sequentially for each time period.

Prophet seeks to eliminate unnecessary calculations but, if required, the time periods for which the variables will be calculated are the maximum projection term. This is from time equal to 0 to time defined by PROJ_TERM_Y * 12, where PROJ_TERM_Y is a mandatory variable in every product.

A set of simple calculations such as those required for using the discounted cashflow technique can be represented as follows:

A group of variables calculated in an ascending time order. These calculations may represent the projection of cashflows.
A group of variables calculated in a descending time order. These calculations may represent the discounting of the projected cashflows.
The above calculations will produce the discounted cashflow value at a fixed point in time, typically the first time period calculated.

Calculation looping
Calculation looping is a process whereby parts of the calculation are repeated several times. In many ways it is similar to the rebasing facility described in the "Rebasing" chapter of this manual. However, calculation looping differs from rebasing in the following ways:

With calculation looping the parts that are repeated are repeated for the whole of the period of calculation. With rebasing only the projected part of the period of calculation is recalculated in each loop.
With calculation looping there is a mechanism to retain some of the values which are calculated in each loop. With rebasing the values which are recalculated in each loop just overwrite the existing values.
An example of the use of this facility is included in the Conventional, International and Unit Linked libraries. In the Conventional and International libraries, the indicator MIN_RESERVE2 allows the valuation reserves to be calculated on several different interest rates by using a different interest rate in each loop. This is needed for resilience reserve calculations because the mathematical reserves need to be calculated on an interest rate which depends on the yields on the matching assets. To estimate the effect of a change in the interest rate, it is necessary to calculate the valuation reserves on at least two interest rates. In the Unit Linked library, the sterling reserves for regular premium pensions business are calculated in one loop assuming premiums continue to maturity and in a second loop assuming that premiums cease immediately.

NO_CALC function

In order to retain values and ensure that they are not overwritten in a subsequent loop, the function NO_CALC is used with the parameter "C".


Each product has an indicator
Each variable has an indicator logic (EG. Is SG_RBC & NTUC_INCOME)
Each product has variables based on the indicator tag

Problem is: Variable A is under scope
Variable A = Variable B + Variable C
Both B and C must be under the product as well
If not under, the product build will fail at runtime >> Because variable B and/or C are missing
Prophet cannot detect this error

Explanation:
Mini Module within Prophet

Similar to VBA > Declare Variables first then can use them later on
EX Formula is NOT a function > Does not return any particular variable
More like a closure where the variables exist within that scope

KEY NOTE (By default) >>>> Extended formulas are NOT t-dependent >>> NOT calculated at every t
Need to declare t as a private variable within the extended formula and use a loop to repeat the calculation
Usually declared as tt >> Avoid confusion with main t

A t-dependent extended formula is similar to normal extended formula except it is re-run for each month of the projection. This effectively makes it t-dependent and allows you to make references to Prophet variables in your extended formula.

The following example is based on the Lookup function extended formula example used to lookup premium allocation rates. Since this formula is only run once for each model point the allocation rate is wrong for a product with an increasing premium. >> Includes t

PUBLIC > Can be referenced by other variables outside the current EX Formula
PRIVATE > Can only be referenced by the current EX Formula
Not case sensitive

Declare array:
1\ NAME(0,0) > Dynamically sized array
2\ NAME(2) > Fixed dimension

Need to declare variable type

Syntax:
Variable Assignment uses ":=" lexical token
<variable>[(indices)] := <expression>

If expression is too long, can use another line using "_"
Avoid having too long lines so that libary comparison tool doesn't screw up

Statements:
IF THEN ELSEIF ELSE END IF
SWITCH CASE CASE ELSE

Loopong
FOR a to z step 1
Do While, do loop while
For Each > Array only

Reference public variables in an extended formula in the form of
EX_FORMULA_NAME.DECLARED_VARIABLE(Dimension, if any)

PRINT TO FILE
Write text/number output to a file on the disk drive
Open Once >

PE
Domain
Workspace Compartment - affects who can see
Workspace Category - Affects how its displayed
Different User Type (EG. Projects Actuary VS RM USer)
Different User Type can access different compartment (EG. RM User Department)
Different Roles can perform different tasks on the workspace (EG. Job Scheduler)
 
8 Machines
Each machine 2 workers
Each worker 64 cores
Total = 8 * 2 * 64 = 512 Cores
1 Core can run one MPF

Look into parallel MPF Processing/Concurrent Batches
Modules

PROJ Result > Y1 is calendar y1

Array Variables
X Dimension
Prophet will calculate the whole thing X times
For non-array variables, the value in that slot will be the Xth loop
Since BE is the last loop, variable values will be the BE loop

Extended formula can print results, but very very big
Certain Death Age
Prophet Debug mode
Pricing model & Recon file link

ILP Reserve Calculation
Regulation says from the valuation date onwards, project using RFR

ILP Reserve Calculation
Regulation says from the valuation date onwards, project using RFR

But reserve at time t+n
means t+0 to t+n grow at BEIR
then after t+n, grow at RFR
Complicated logic needs EX Formula

Same for calculating forward rates, need to rebase in each period, so need EX formula

Renewable Term Products
EG Term for 10 years, can renew

More conservative to assume that the PH will not renew
However, if want to model renewability, cannot assume that all will renew - need assume a good chunk of them never renew (Mass Lapse on renewal date)

Lapse Supported Product
Meaning that lapse is good for the policyholder
Term product
Lapse in the early years is bad, cant recoup the cost of the policy
Lapse in the later years is good, collect the money but never pay any benefits

If got surrender benefit, then need see relative size of surrender benefit


Master Product
Expression
Picks up variables according to the expressions

Overriding comm hard to model because it depends on the distribution structure
Agent -> Manager
Maneger -> Head
Agent -> Head

Usually MPF no granulaity