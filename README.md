# Fractal-ordinal-market-AMM
This is an Automatic market maker for Ordinal Marketplace built on the Fractal Bitcoin network. Users can list their ordinals on this market, and buyers can purchase or place orders for listed ordinals based on ordinal theory within the Fractal ecosystem.

## Overview

- **Network:** Fractal Bitcoin
- **Functionality:** Listing, purchasing, and managing ordinals based on ordinal theory
- **Documentation:** Swagger integrated for API documentation

## Setup and Configuration  

### Prerequisites 

- Ensure Node.js is installed. 
- Create an `.env` file using `.env.example` as a reference.

### Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/solguru310/fractal-ordinal-AMM.git
    cd fractal-ordinalt-AMM
    ```
2. Install project dependencies:
    ```bash
    npm install
    ```
3. Configure environment variables in `.env`:
    ```plaintext
    NETWORKTYPE=TESTNET
    PORT=3000
    MONGODB_URI=mongodb://localhost:27017/fractal-ordinal-AMM
    ```
4. Launch the server:
    ```bash
    npm start
    ```

## Application Usage

Once the server is started, access the server on the specified port (default: 3000). The API documentation is available via Swagger UI at `http://localhost:3000/api-docs`.

## API Endpoints

### Listing Management
- **Create Listing**: `/api/create-listing`  
  Method: `POST`  
  Functionality: Lists ordinals for sale on Fractal network; responds with a Partially Signed Bitcoin Transaction (PSBT).

- **Save Listing**: `/api/save-listing`  
  Method: `POST`  
  Functionality: Saves a signed PSBT in the listings database.

- **Relist**: `/relist`  
  Method: `POST`  
  Functionality: Updates listing price with a new PSBT requiring the seller's signature.

- **Confirm Relist**: `/confirm-relist`  
  Method: `POST`  
  Functionality: Confirms updated price with a signed PSBT.

- **Delist**: `/delist`  
  Method: `POST`  
  Functionality: Removes ordinals from listing and returns them to the seller.

### Offer Management
- **Create Offer**: `/api/create-offer`  
  Method: `POST`  
  Functionality: Creates a transaction for purchasing ordinals; includes a platform fee upon success.

- **Submit Offer**: `/api/submit-offer`  
  Method: `POST`  
  Functionality: Completes a purchase with a signed PSBT, incurring a 1% platform fee on the seller.

## MongoDB Schema

- Integrated MongoDB schema design to support listing and offer operations, ensuring efficient database interactions.

## Contact me
If you need more technical support and development inquires, you can contact below.

Telegram: [@dwlee918](https://t.me/@dwlee918)

X: [@derricklee918](https://x.com/derricklee918)

Discord: [@solGuru](https://discordapp.com/users/352387576017190913)

Thanks.
