# Auto Refuel Application

## Overview
Auto Refuel is a web application designed to facilitate the online ordering and delivery of various fuel types directly to your location. It integrates a seamless payment system using Stripe and provides a user-friendly interface for selecting fuel types, specifying quantities, and confirming orders.

## Features
- **Fuel Selection**: Users can choose from various types of fuel and specify the quantity in liters.
- **Dynamic Pricing**: The application calculates the total cost based on the selected fuel type and quantity, including delivery charges.
- **Secure Payment**: Integrates with Stripe for secure payment processing.
- **Responsive Design**: Compatible with various devices, ensuring a smooth user experience.

## Technologies Used
- **React**: For building the user interface.
- **Next.js**: A React framework for server-side rendering and generating static websites.
- **Stripe**: For handling payments.
- **Tailwind CSS**: For styling and designing the frontend.
- **Prisma**: As an ORM for handling database operations.
- **TypeScript**: For adding static type definitions to JavaScript.
- **MongoDB**: For Database 

## Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/ciobiano/AutoRefuel.git
   cd auto-refuel
   ```

2. **Install dependencies**
   ```bash
   pnpm install
   ```

3. **Set up environment variables**
   - Rename `.env.example` to `.env`.
   - Fill in the necessary API keys and database credentials.

4. **Run the development server**
   ```bash
   pnpm  dev
   ```

## Usage

Navigate to `http://localhost:3000` to access the application. From the homepage, users can:
- Select the type of fuel and specify the quantity.
- View the calculated costs including delivery fees.
- Proceed to checkout and complete the payment.

## API Reference

### Create Payment Intent
**POST** `/api/create-intent`
- **Body**:
  ```json
  {
    "fuelType": "Gasoline",
    "liters": 10,
    "amount": 8200
  }
  ```
- **Response**:
  ```json
  {
    "client_secret": "secret_key_here"
  }
  ```

## Contributing

Contributions are welcome! Please fork the repository and create a pull request with your features or fixes.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

