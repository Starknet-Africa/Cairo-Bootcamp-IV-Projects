# TipMeme - Cairo Bootcamp IV Project Submission

## Project Name
TipMeme

## Project Description
TipMeme is an innovative Web3 tipping platform built on Starknet that seamlessly integrates with social media platforms, starting with Twitter. It enables creators to receive tips in cryptocurrency (ETH/STRK) directly through a Chrome extension, with features like gasless transactions and a comprehensive creator dashboard.

### Key Features
- 🎯 **Chrome Extension**: Seamlessly inject tip buttons into Twitter profiles
- 💸 **Multi-Token Support**: Send tips in ETH or STRK
- ⚡ **Gasless Transactions**: Users can tip without paying gas fees
- 📊 **Creator Dashboard**: Complete analytics and withdrawal management
- 🔐 **Secure Wallet Integration**: Support for ArgentX and Braavos
- 🏆 **Social Features**: Leaderboards and tip history

### Technical Stack
- **Smart Contracts**: Cairo (Starknet)
- **Frontend**: Next.js, TypeScript, Tailwind CSS
- **Backend**: Node.js Paymaster Service
- **Extension**: Chrome Extension API
- **Deployment**: Vercel (Frontend), Render.com (Paymaster)

## Project Category
SocialFi & DeFi

## Project Links
- **Live Demo**: [tipmeme.vercel.app](https://tipmeme.vercel.app)
- **Project Video**: [YouTube Demo](https://youtu.be/39Rvr8Kvv5w)
- **Codebase**: [GitHub Repository](https://github.com/big14way/Tipmeme.git)

## Project Architecture

```
📦 TipMeme
├── 🌐 app/                          # Next.js frontend
├── 🧩 chrome-extension/             # Twitter integration
├── 🎨 components/                   # React components
│   ├── 📊 dashboard/               # Creator dashboard UI
│   └── 🎯 ui/                      # Shared components
├── 📜 src/                         # Cairo contracts
├── 🧪 tests/                       # Contract tests
├── 🛠️ paymaster-service/           # Gasless transaction service
└── 📚 Documentation/               # Guides & docs
```

## Smart Contract Features
- **Secure Tipping**: Validated transaction processing
- **Multi-token Support**: Handle both ETH and STRK
- **Gasless Operations**: Paymaster integration
- **Access Control**: Role-based permissions
- **Event Emission**: Detailed transaction tracking

## Technical Innovations
1. **Advanced Paymaster Service**
   - Rate limiting for security
   - Multi-token sponsorship
   - Comprehensive transaction validation

2. **Seamless Social Integration**
   - Non-intrusive UI injection
   - Real-time price conversion
   - Automatic wallet detection

3. **Creator-Centric Dashboard**
   - Real-time analytics
   - Visual earnings tracking
   - Automated withdrawal system

## Future Roadmap
- 📱 Mobile app development
- 🌍 Support for additional social platforms
- 💎 NFT tipping integration
- 🏪 Creator marketplace
- 🤖 AI-powered tip recommendations

## Team/Individual Information
- **Developer**: Godswill
- **Role**: Solo Developer
- **Contact**: [GitHub Profile](https://github.com/big14way)

## Development Status
- ✅ Smart Contracts Deployed
- ✅ Frontend Live
- ✅ Chrome Extension Ready
- ✅ Paymaster Service Operational

## Additional Resources
- Comprehensive documentation in repository
- Detailed deployment guides
- Testing guides for all components
- Security considerations and best practices

---

*Built with ❤️ on Starknet for the Cairo Bootcamp IV* 