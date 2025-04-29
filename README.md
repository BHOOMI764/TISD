# 🌍 FootprintX

FootprintX is a sustainable web application aligned with **UN SDG Goal 13: Climate Action**. It empowers users to **monitor**, **act**, and **engage** in reducing their carbon footprint, while enabling a marketplace for **reusable goods** and providing a **complaint redressal portal** that bridges citizens with government departments.

---

## 📌 Features

### 1. 🔢 Carbon Footprint Calculator
- Converts user input into estimated **annual CO2e emissions** using simplified formulas.
- Metrics considered:
  - **Transportation** (daily km)
  - **Energy usage** (monthly kWh)
  - **Waste** (weekly kg)
  - **Shopping** (monthly expenditure)
  - **Flights** (annual hours)
- Reference Sources:
  - [UK Government Conversion Factors (2023)](https://www.gov.uk/government/publications/greenhouse-gas-reporting-conversion-factors-2023)
  - [EPA GHG Equivalencies Calculator](https://www.epa.gov/energy/greenhouse-gas-equivalencies-calculator)

### 2. 🛠 Complaint Portal
- Users can file complaints to relevant departments using a form-based interface.
- Fields include department, title, message, tweet content, tagged users, and optional image.
- Tweet simulation with console log.
- Protected with AuthGuard for authenticated submissions.
- Toast notifications via `sonner`.

### 3. ♻️ Reusable Item Platform
- **Buy, Sell, or Claim** reusable items.
- Clean user interface for item listing.
- Real-time claim system implemented via `claimController.js`.

### 4. 🔄 Item Swapping
- Users can swap reusable goods with others.
- Enables community-based reuse and circular economy participation.

---

## 🚀 Tech Stack

- **Frontend**: React.js, Tailwind CSS
- **Backend**: Node.js, Express.js
- **Database**: Sequelize + MySQL
- **Authentication**: JWT-based
- **Image Upload**: `react-dropzone` (UI ready, backend pending)
- **Notifications**: `sonner`

---

## 🧠 Algorithms Used

### Carbon Footprint Calculation
```js
transportationScore = transportation * 0.2 * 365
energyScore = energy * 0.5 * 12
wasteScore = waste * 0.7 * 52
shoppingScore = shopping * 0.1 * 12
flightsScore = flights * 90
totalEmissions = transportationScore + energyScore + wasteScore + shoppingScore + flightsScore
scoreForLeaderboard = Math.round(totalEmissions)
