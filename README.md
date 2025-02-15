# Exam-Q4



The program is organized into different classes which represents households, devices, and data plans.

### Household Class:

##### Attributes:
- `List<Device> devices`
- `DataPlan plan`

#### Methods:
- `calculateTotalBill()`: calculates total bill based on plan type, devices, and additional fees.
- `applyDiscounts()`: applies any bundle discounts.

### Device Class:

##### Attributes:
- `String deviceName`
- `double dataUsageGB`
- `DeviceType type` (enum: broadband, mobile)

#### Methods:
- `getDataUsage()` : returns device's data consumption.

### dataPlan:

##### Attributes:
- `double baseCost`
- `double speedTier (for Unlimited Plans)`
- `boolean isUnlimited`
- `double dataCapGB (only for Fixed Plans)`
- `double overageChargePerGB`
- `double deviceCharge`

#### Methods:
- `calculatePlanCost(Household household)`: calculates base cost, device fees, and overage.

### Concrete Plan Classes
`FixedDataPlan`
`UnlimitedPlan`
`DeviceBasedPlan`
`PerDeviceFixedPlan`

each implements `calculatePlanCost()` differently based on plan type.



### User interaction:
Users input:
1. Selected data plan and its details
2. Household devices and their data usage

System outputs:
1. Base cost breakdown
2. Device-based charges
3. Overage fees (if applicable)
4. Total bill




























