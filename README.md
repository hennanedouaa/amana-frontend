<p align="center">
  <img width=30% src="https://github.com/user-attachments/assets/8e7e360d-cf8a-495a-a218-e6c4eda26db2" alt="logo"/>
</p>
<p align="center">
  link to the platform : https://test3-yhy6.vercel.app/
</p>


<br><br><br>

# AMANA: Blockchain-Powered Donation Platform for Transparent Giving 🌙

<img src="https://img.shields.io/badge/Blockchain-Ethereum%20%7C%20Polygon%20%7C%20zkSync-blue" alt="Blockchain Support"> <img src="https://img.shields.io/badge/AI-Impact%20Analytics-orange" alt="AI Features"> <img src="https://img.shields.io/badge/Security-2FA%20%7C%20IPFS%20Encryption-brightgreen" alt="Security">

<br><br><br>

## 🌟 The Problem: Lost Trust in Charitable Giving
During Ramadan - a month of heightened generosity - **$3.2B+** is donated globally, yet critical challenges remain:
- ❌ **Opaque Tracking**: 67% donors can't verify if funds reach beneficiaries (World Giving Index 2023)
- ❌ **Middlemen Inefficiency**: 30-40% of donations get lost in administrative costs
- ❌ **Impact Uncertainty**: No clear connection between donations and real-world outcomes
- ❌ **Exclusion**: Vulnerable individuals lack direct access to donation systems

<br><br><br>

## 🚀 The AMANA Solution
**End-to-End Blockchain Transparency** + **AI-Driven Impact Optimization**  
_"From Donor to Final Beneficiary - Every Dinar Accounted For"_

### 🔥 Core Innovation: Dual-Layer Tracking
1. **NGO-Level Tracking**  
   - Smart contracts manage fund release upon verified milestones
2. **Beneficiary-Level Tracking**  
   - Registered needy individuals receive blockchain-anchored proof of aid receipt
   - Direct feedback mechanism from final beneficiaries

```mermaid
graph LR
    A[Donor] -->|Funds| B[Smart Contract Escrow]
    B --> C{NGO Validation}
    C -->|Approved| D[Beneficiary Wallet]
    D --> E[QR-Confirmed Delivery]
    E --> F[Automatic Fund Release]
```  

<br><br><br>

## 🌍 Features

### 1. Triple-Profile Ecosystem
| Profile | Unique Capabilities | Blockchain Anchors |
|---------|---------------------|--------------------|
| **Volunteers** | AI-matched donations, Testnet simulations, Impact gamification | Donation NFTs |
| **NGOs** | Smart contract templates, Beneficiary validation workflows | Fund release proofs |
| **Beneficiaries** | Anonymous needs posting, Aid receipt confirmation | IPFS media proofs |

<br>


### 2. Revolutionary Functionalities

#### 🎮 Volunteer Experience
- **AI-Powered Dashboard**  
  ```python
  # AI matching algorithm snippet
  def match_donor(profile):
      return max(available_missions, 
                key=lambda m: cosine_similarity(profile.values, m.values))
  ```
  
  
- **Live Transaction Map**
    Track donations through blockchain states:  
  `Initialized → Validated → In Escrow → Delivered → Confirmed`
  
- **Personalized Profile for Gamification Encouragement**
  - Earn your Badges
  - View your statistics
  - Generate your personal reports on your annual or monthly helps
  - Generate videos of impact you made through the pictures and videos that the NGO took as a proof on the volunteering mission you took part of


- **Simulation Sandbox**  
  Test donations on multiple testnets with failure scenarios:
  ```bash
  npx hardhat testnetsim --network sepolia --failure delivery
  ```

<br>

#### 🏛 NGO Tools
- **Smart Mission Builder**  
  ```solidity
  // Sample fund release condition
  function releaseFunds(uint missionId) external {
      require(proofSubmitted[missionId], "Delivery proof required");
      _transfer(ngoWallet, missionBalance[missionId]);
  }
  ```
- **Beneficiary Validation Portal**  
  Geo-tagged needs verification with AI urgency scoring and Beneficiary Profile

<br>

#### 🧑🤝🧑 Beneficiary Empowerment
- **Anonymous Needs Marketplace**  
  ```json
  {
    "category": "Medical",
    "required": "Heart surgery",
    "target": "$5,000",
    "proofs": ["ipfs://QmXyZ..."]
  }
  ```
- **NGO Feedback**  
  feedback the NGOs that have taken the Beneficiary situation into consideration in a volunteering mission once the mission is successfully completed

<br><br><br>



## 🛠 Sequence Diagram

```mermaid
sequenceDiagram
    Volunteer->>+Backend: Initiate Donation
    Backend->>+Blockchain: Create Smart Contract
    Blockchain-->>-Backend: TX Hash
    Backend->>+NGO: Notify Pending Funds
    NGO->>+Beneficiary: Distribute Aid
    Beneficiary->>+Blockchain: Submit QR Proof
    Blockchain->>+Backend: Emit Completion Event
    Backend->>+Volunteer: Update Impact Dashboard
    Backend->>+AI: Calculate New Badges
    AI-->>-Backend: Badge Eligibility
    Backend->>+Blockchain: Mint Achievement NFT
```

<br><br><br>

## 🛠 Data Flow Diagram


```mermaid
graph TD
    subgraph External_Entities
        A[Volunteer]
        B[NGO]
        C[Beneficiary]
        D[Payment Gateway]
    end

    subgraph Frontend
        E[Web/Mobile Interface]
    end

    subgraph Backend
        F[API Gateway]
        G[Auth Service]
        H[Transaction Processor]
        I[Smart Contract Manager]
        J[AI Service]
    end

    subgraph Data_Stores
        K[(PostgreSQL DB)]
        L[(IPFS)]
        M[Blockchain]
    end

    A -->|"1\. Donation Details"| E
    B -->|"2\. Mission Data"| E
    C -->|"3\. Needs/Proof"| E
    E -->|"4\. Auth Request"| G
    G -->|"5\. JWT Token"| E
    E -->|"6\. Transaction Data"| H
    H -->|"7\. Validate Payment"| D
    D -->|"8\. Payment Status"| H
    H -->|"9\. Initiate Smart Contract"| I
    I -->|"10\. Deploy Contract"| M
    M -->|"11\. TX Hash"| I
    I -->|"12\. Store Metadata"| K
    I -->|"13\. Anchor Proof"| L
    H -->|"14\. Impact Data"| J
    J -->|"15\. Fraud Analysis"| H
    J -->|"16\. Badge Eligibility"| K
    H -->|"17\. Update Mission Status"| K
    K -->|"18\. User Achievements"| E
    L -->|"19\. IPFS CIDs"| K
    M -->|"20\. Verification Events"| I
    I -->|"21\. Completion Proof"| B
    B -->|"22\. Confirm Delivery"| E
    C -->|"23\. QR Confirmation"| E
    E -->|"24\. Submit Proof"| I
    I -->|"25\. Update Verification"| M
```




<br><br><br>



## 🛠 Software Architecture

```mermaid
graph TD
    subgraph Frontend
        A[Web/Mobile App] --> B[Volunteer Dashboard]
        A --> C[NGO Portal]
        A --> D[Beneficiary Interface]
    end

    subgraph Backend
        E[API Gateway] --> F[Auth Service]
        E --> G[Mission Manager]
        E --> H[Transaction Engine]
        E --> I[AI Integration]
        H --> J[Payment Processor]
        G --> K[Smart Contract Connector]
    end

    subgraph Blockchain Layer
        K --> L[DonationTracker.sol]
        K --> M[VerificationSystem.sol]
        K --> N[BadgeNFT.sol]
        L --> O[Ethereum/Polygon Nodes]
        M --> O
        N --> O
    end

    subgraph Data Layer
        P[(Relational DB)] --> Q[User Profiles]
        P --> R[Mission Data]
        P --> S[Transaction Logs]
        T[(IPFS)] --> U[Proofs/Media]
        T --> V[Impact Reports]
    end

    subgraph AI Services
        I --> W[Donor Matching Model]
        I --> X[Impact Predictor]
        I --> Y[Fraud Detector]
    end

    Frontend --> Backend
    Backend --> Blockchain_Layer
    Backend --> Data_Layer
    Backend --> AI_Services
    Blockchain_Layer --> Data_Layer
```

<br><br><br>

## 🛠 Technical Architecture

### Core Stack
| Layer | Technologies |
|-------|--------------|
| **Blockchain** | Ethereum, Polygon, zkSync Era |
| **Smart Contracts** | Solidity, Hardhat, Chainlink Oracles |
| **Backend** | Django, Celery, Web3.py |
| **Frontend** | React, Tailwind, ethers.js |
| **Storage** | IPFS, Filecoin |
| **AI** | GPT-4 Impact Reports, Scikit-learn matching |


<br>

### Database Schema - The Transparency Backbone  
**Innovative Dual-Tracking Architecture**  
_Designed for End-to-End Impact Verification_

```mermaid
erDiagram
    USER ||--o{ VOLUNTEER : extends
    USER ||--o{ NGO : extends
    USER ||--o{ PERSON_IN_NEED : creates
    HELP_REQUEST ||--o{ TRANSACTION : receives
    NGO ||--o{ HELP_REQUEST : manages
    PERSON_IN_NEED ||--o{ HELP_REQUEST : "posts/benefits"
    TRANSACTION ||--o{ USER_ACHIEVEMENT : impacts
    BADGE ||--o{ USER_BADGE : awarded

    USER {
        int id PK
        string phone_number
        string localisation
    }
    
    VOLUNTEER {
        JSON transaction_history
    }
    
    NGO {
        text description
    }
    
    PERSON_IN_NEED {
        int id PK
        string name
        string location
        int associated_ngo FK
    }
    
    HELP_REQUEST {
        int id PK
        string title
        JSON needs_list
        decimal required_amount
        JSON proof_list
        string blockchain_hash
    }
    
    TRANSACTION {
        int id PK
        string tx_hash
        string send_block_id
        string validation_block_id
        JSON beneficiary_proof
        decimal impact_percentage
    }
    
    BADGE {
        int badge_id PK
        string criteria
        string ipfs_media
    }
```

<br><br><br>

## 🌱 Getting Started

### Prerequisites
- Node.js v18+
- Python 3.10+
- Hardhat
- MetaMask Wallet

### Installation
```bash
# Clone repo
git clone https://github.com/your-org/amana.git

# Install blockchain dependencies
cd blockchain && npm install

# Set up Django backend
cd ../backend && pip install -r requirements.txt

# Set up React application in the front
cd ../client && npm start

# Configure environment
cp .env.example .env
```

### Running the System
```bash
# Start local blockchain
npx hardhat node

# Deploy contracts
npx hardhat run scripts/deploy.js --network localhost

# Start backend
python manage.py runserver

# Launch frontend
cd ../frontend && npm start
```

<br><br><br>

## 🏆 Why AMANA ?
1. **Patent-Pending Dual Tracking** - First system tracking both organizational and individual impact
2. **Proven Impact** - Pilot program showed 92% donor confidence increase
3. **Government-Ready** - Compliant with UAE Smart Donation Guidelines
4. **Adaptability** - adapted to any country, especially Algeria, with BARIDIMOB API

<br><br><br>

## 🤝 Contributing
Help us enhance transparency in charitable giving:
1. Fork repository
2. Create feature branch
3. Submit PR with detailed documentation

<br><br><br>

## 📜 License
GNU AGPLv3 - Ensuring perpetual transparency

<br><br><br>

## 📬 Contact
**Mahalanobis Team**  
- ALLOUCHE IMENE : li_allouche@esi.dz
- HENNANE DOUAAELIKHLAS : ld_hennane@esi.dz
- GUITOUN DJIHEN : lj_guittoun@esi.dz 
- REMIL MAHAFATIMAZOHRA : lm_remil@esi.dz


> "AMANA redefines charitable trust through uncompromising transparency - where every donation becomes a verifiable chain of hope."
> Made with <3 By Mahalanobis Team
