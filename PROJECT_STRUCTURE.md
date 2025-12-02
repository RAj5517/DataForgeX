# DataForgeX - Project Structure

Complete monorepo structure for the Privacy-First AI + Web3 Data Marketplace.

```
DataForgeX/
├── .gitignore                 # Git ignore patterns
├── .env.example               # Environment variables template
├── package.json               # Root workspace configuration
├── README.md                  # Main project documentation
├── PROJECT_STRUCTURE.md       # This file
│
├── frontend/                  # Next.js + TypeScript Frontend
│   ├── pages/                 # Next.js pages/routes
│   ├── components/            # Reusable React components
│   ├── lib/                   # Utility functions
│   ├── encryption/            # Client-side encryption utilities
│   └── README.md
│
├── backend/                   # FastAPI Python Backend
│   ├── app/
│   │   ├── routes/            # API route handlers
│   │   ├── models/            # Database models (SQLAlchemy)
│   │   ├── database/          # DB configuration & migrations
│   │   └── utils/             # Utility functions
│   ├── blockchain_listener.py # Smart contract event listener
│   └── README.md
│
├── contracts/                 # Solidity Smart Contracts
│   ├── Marketplace.sol        # Main marketplace contract
│   ├── test/                  # Contract tests
│   ├── scripts/               # Deployment scripts
│   └── README.md
│
├── ml/                        # AI Inference Engine
│   ├── inference.py           # Main inference service
│   ├── models/                # Saved model files (gitignored)
│   ├── requirements.txt       # Python dependencies
│   └── README.md
│
├── infra/                     # Infrastructure & Deployment
│   ├── docker-compose.yml     # Local dev environment
│   ├── deployment/            # Production deployment configs
│   └── README.md
│
└── shared/                    # Shared Code
    ├── types/                 # TypeScript/Python type definitions
    └── README.md
```

## Directory Purposes

### frontend/
Next.js application handling:
- Wallet connection (wagmi)
- Client-side file encryption
- IPFS upload UI
- Listing creation and browsing
- Purchase flow
- AI result viewing
- User dashboard

### backend/
FastAPI server providing:
- User authentication (wallet signature verification)
- Listing registration API
- Purchase event processing
- Access grant management
- AI inference endpoints
- Database operations
- Blockchain event listening

### contracts/
Smart contracts deployed on Base:
- Marketplace contract (listings, purchases, access control)
- Event emissions for audit trail
- USDC payment handling

### ml/
AI model inference:
- Text summarization
- Data insights extraction
- Secure model loading and execution

### infra/
Deployment configurations:
- Docker Compose for local development
- Cloud deployment configs (Cloud Run, ECS, etc.)
- CI/CD pipelines

### shared/
Code shared between frontend and backend:
- Type definitions
- Constants
- Validation schemas

## Next Steps

See the main README.md for the complete development roadmap.

Phase 0.1 Complete ✅ - Repository structure is ready!

