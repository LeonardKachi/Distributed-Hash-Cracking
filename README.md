# DistributedHashCracker

> On-demand, distributed hash cracking using your own cloud infrastructure

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Contributions Welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat)](CONTRIBUTING.md)
[![Security Focus](https://img.shields.io/badge/focus-security%20research-blue)](docs/SECURITY.md)

## What is this?

DistributedHashCracker is an open-source platform that revolutionizes cryptographic hash cracking by enabling distributed computing across user-supplied cloud infrastructure. Instead of being limited to single machines or expensive centralized services, researchers can now leverage their own AWS accounts for scalable, cost-effective parallel hash cracking.

## The Problem We Solve

Current hash cracking solutions face critical limitations:
- **Single Machine Bottlenecks**: Desktop tools limited by local hardware
- **Expensive Services**: Centralized platforms with high operational costs
- **Trust Issues**: Security researchers hesitant to use black-box services
- **Scale Limitations**: No easy way to distribute workload across hundreds of containers

## Our Solution

Submit a hash through our web interface, configure your AWS credentials and resource preferences, then watch as the platform automatically:

- Provisions distributed compute infrastructure via Terraform
- Deploys containerized hash cracking engines
- Intelligently divides the search space across all containers
- Provides real-time progress monitoring and cost tracking
- Automatically cleans up resources when complete

## Key Features

🚀 **Dynamic Scaling** - From single containers to hundreds of instances  
💰 **Cost Control** - Use your own AWS account, set strict budget limits  
🔍 **Smart Distribution** - Optimal work allocation reduces cracking time  
📊 **Real-time Monitoring** - Live progress tracking and performance metrics  
🔒 **Security First** - Open source, minimal permissions, credential isolation  
🎯 **Multi-Algorithm** - MD5, SHA-1, SHA-256, NTLM, and more  

## Architecture Overview

```
User Interface → Job Queue → Terraform Provisioning → Container Orchestration
                                        ↓
Results ← Progress Aggregation ← Distributed Hash Cracking ← Work Distribution
```

The platform uses a coordinator-worker pattern where a central service distributes work chunks to containerized crackers, automatically handling failures and load balancing.

## Use Cases

### Security Research
Academic and commercial cryptographic analysis with scalable compute resources

### Penetration Testing
Client engagement password recovery with controlled costs and transparent processes

### Digital Forensics
Evidence recovery and analysis with distributed processing capabilities

### Educational Applications
Cryptography courses demonstrating hash vulnerabilities and distributed computing concepts

## Quick Start

**Prerequisites:**
- AWS Account with appropriate permissions
- Basic understanding of hash cracking concepts
- Modern web browser

**Steps:**
1. Clone this repository
2. Configure your AWS credentials following our security guide
3. Submit a hash via the web interface
4. Monitor progress and retrieve results

*Full deployment documentation coming soon*

## Project Status

🚧 **Currently in Development** 🚧

We're actively building the core platform components:

- ✅ Technical specification complete
- 🔄 Frontend web application (in progress)
- 🔄 Backend API service (in progress)
- 📋 Terraform infrastructure templates (planned)
- 📋 Container orchestration system (planned)

## Contributing

We welcome contributions from security researchers, cloud engineers, and cryptography enthusiasts. This project needs expertise in:

- **Frontend Development**: React/Vue.js for user interface
- **Backend Engineering**: API design and job management systems
- **DevOps/Infrastructure**: Terraform, AWS, container orchestration
- **Cryptography**: Hash cracking algorithms and optimization
- **Security**: Credential management, audit procedures

See our [Contributing Guide](CONTRIBUTING.md) for detailed information.

## Security Considerations

This platform is designed for legitimate security research, penetration testing, and educational purposes. Users are responsible for:

- Ensuring legal compliance in their jurisdiction
- Using only authorized hash values
- Implementing appropriate access controls
- Following responsible disclosure practices

See our [Security Policy](docs/SECURITY.md) for complete guidelines.

## Community

- **Discussions**: Use GitHub Discussions for questions and ideas
- **Issues**: Report bugs and feature requests via GitHub Issues
- **Security**: Contact security@distributedashcracker.com for vulnerabilities
- **Updates**: Follow [@DistHashCrack](https://twitter.com/DistHashCrack) for development updates

## Roadmap

### Phase 1 (Next 3 Months)
- MVP web interface and basic API
- Single-algorithm support (MD5)
- Manual infrastructure management

### Phase 2 (Months 4-6)
- Multi-algorithm support
- Automatic resource cleanup
- Real-time progress monitoring

### Phase 3 (Months 7-9)
- GPU acceleration support
- Advanced attack modes (dictionary, hybrid)
- Performance analytics

### Phase 4 (Months 10-12)
- Enterprise features and API access
- Multi-cloud support (Azure, GCP)
- Advanced reporting and compliance

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Inspired by the need for accessible, transparent distributed computing in security research
- Built on the shoulders of excellent open-source tools like Hashcat and John the Ripper
- Grateful to the security research community for their continued innovation

## Support

If you find this project valuable, please:
- ⭐ Star this repository
- 🐛 Report issues you encounter  
- 💡 Suggest new features
- 📢 Share with your network
- 🤝 Contribute code or documentation

---

**Disclaimer**: This tool is intended for authorized security research and testing only. Users are solely responsible for ensuring compliance with applicable laws and regulations.
