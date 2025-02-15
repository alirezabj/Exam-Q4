# Exam-Q4



The program is organized into different classes which represents households, devices, and data plans.

1. Households: Represents a home with devices and a selected data plan.
2. Devices: Represents different types of internet-connected devices (broadband or mobile).
3. Data Plans: Represents different internet subscription plans with specific pricing structures.


### Household Class:

##### Attributes:
- `List<Device> devices`: a list of devices such as laptops, phones, and tablets in the household
- `DataPlan plan`: the selected internet plan for the household

#### Methods:
- `calculateTotalBill()`: calculates total bill based on plan type, number and type of devices, and additional fees
- `applyDiscounts()`: applies any bundle discounts

### Device Class:

##### Attributes:
- `String deviceName`: the name of the device
- `double dataUsageGB`: how much data the device has consumed
- `DeviceType type`: whether the device uses broadband or mobile data

#### Methods:
- `getDataUsage()` : returns how much data the device has consumed

### dataPlan:

##### Attributes:
- `double baseCost`: the fixed cost of the plan
- `double speedTier (for Unlimited Plans)`: extra charge for higher internet speeds
- `boolean isUnlimited`: true if the plan has no data cap otherwise false if it does
- `double dataCapGB (only for Fixed Plans)`: the maximum data limit
- `double overageChargePerGB`: extra charge per GB if the user exceeds their data limit
- `double deviceCharge`: additional charges per device if applicable

#### Methods:
- `calculatePlanCost(Household household)`: calculates base cost, device fees, and overage fees if applicable

### Concrete Plan Classes

Each subclass inherits from `DataPlan` and implements `calculatePlanCost()` differently

`FixedDataPlan`: has a monthly data cap and charges extra fees if the user exceeds the cap
`UnlimitedPlan`: no data cap and the users choose a speed tier which affects cost
`DeviceBasedPlan`: a base plan cost with extra charges per connected device
`PerDeviceFixedPlan`: similar to FixedDataPlan, but applies separate data limits for each device.



### User interaction:
Users input:
1. selects a data plan
2. enters household devices: device type (broadband or mobile), device name (paptop or phone or tablet), device usage (how much GB the device has consumed)

System outputs:
1. base plan cost: the starting price of the selected plan
2. device-based charges: Extra fees for each device if applicable
3. overage fees: additional charges if data limits are exceeded
4. total bill: the final price the household needs to pay




























