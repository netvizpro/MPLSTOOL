# MPLS Network Configuration Tool Suite

A comprehensive web-based toolset for generating production-ready MPLS configurations with visual topology diagrams and automated Python scripts.

## Overview

This tool helps network engineers quickly generate accurate MPLS configurations for common deployment scenarios. All processing is done locally in your browser - no data is sent to external servers.

## Features

### 1. VRF Route-Target Analyzer
- Analyzes VRF configurations and route-target relationships
- Visual traffic flow diagrams showing import/export paths
- Supports both IOS and IOS-XE formats
- Real-time validation and error checking

### 2. L2VPN xConnect Generator
- Point-to-point Layer 2 VPN configurations
- Pseudowire-class based setup
- Both PE router configs generated simultaneously
- Interactive network topology diagram
- Complete verification commands included

**Configuration includes:**
- Pseudowire class definitions
- Interface xConnect commands
- MPLS LDP base configuration
- Troubleshooting commands

### 3. MPLS Traffic Engineering Generator
- Dual-tunnel topology with automatic path selection
- Visual network diagram showing tunnel paths
- Explicit path configurations via P routers
- Auto-bandwidth and Fast Reroute support

**Key capabilities:**
- **Tunnel 1** (Primary): Direct path via P1 (TE metric: 100)
- **Tunnel 2** (Preferred): Optimized path via P2-P3 (TE metric: 50)
- Complete PE and P router configurations
- OSPF-TE extensions included
- RSVP bandwidth reservation

### 4. Python Script Generation
Every configuration template includes a downloadable Python script that:
- Generates identical configurations offline
- Supports CSV bulk imports
- Interactive CLI mode with sensible defaults
- Validates input parameters

## Quick Start

1. **Open the tool**: Load `index.html` in any modern web browser
2. **Select your template**: Choose from L2VPN, MPLS-TE, or QoS generators
3. **Fill in parameters**: Enter your network details (defaults provided)
4. **Generate config**: Click the generate button
5. **Copy or download**: Use the generated configuration in your network

## L2VPN xConnect Example

```
PE1 Configuration:
  Router Name: Green
  Loopback: 10.10.10.1
  Interface: GigabitEthernet1/0/1

PE2 Configuration:
  Router Name: Blue
  Loopback: 10.10.10.2
  Interface: GigabitEthernet1/0/1

VC ID: 10007
```

Generates complete xConnect configuration for both routers with proper pseudowire-class setup.

## MPLS-TE Dual Tunnel Example

```
PE1 Router: 1.1.1.1
PE2 Router: 2.2.2.2
Tunnel 1: 100 Mbps bandwidth
Tunnel 2: 50 Mbps bandwidth (preferred path)
```

Automatically creates:
- Two TE tunnels with explicit paths
- Complete P router configurations
- Auto-bandwidth settings
- Fast Reroute protection

## Configuration Output

All generated configurations include:

✓ **Complete router commands** - Ready to paste into CLI  
✓ **Verification commands** - Test your deployment  
✓ **Troubleshooting commands** - Debug issues quickly  
✓ **Configuration notes** - Best practices and warnings  
✓ **Timestamp** - Track when configs were generated

## Security & Privacy

- **100% client-side processing** - All code runs in your browser
- **No data transmission** - Nothing is sent to external servers
- **No login required** - Use immediately without accounts
- **Offline capable** - Works without internet after initial load

## Browser Requirements

- Chrome/Edge 90+
- Firefox 88+
- Safari 14+
- Any modern browser with JavaScript enabled

## Use Cases

### Service Provider Networks
- L2VPN circuit provisioning
- MPLS-TE optimization for critical traffic
- Bulk configuration generation via Python scripts

### Enterprise Networks  
- Multi-site connectivity with L2VPN
- QoS policy standardization
- Network migration planning

### Network Engineers
- Quick configuration templates
- Learning MPLS technologies
- Lab environment setup

## Tips for Best Results

1. **Start with defaults** - Pre-filled values follow best practices
2. **Review generated configs** - Always validate before deployment
3. **Use verification commands** - Included in every config output
4. **Download Python scripts** - For repetitive tasks or bulk deployments
5. **Check metric values** - TE metrics determine path selection

## MPLS-TE Path Selection

The tool automatically configures intelligent path selection:

- **Lower TE metric = preferred path**
- Tunnel 2 (TE: 50) selected before Tunnel 1 (TE: 100)
- Dynamic path-option provides backup if explicit path fails
- Auto-bandwidth adjusts based on actual traffic patterns

## Configuration Standards

All generated configurations follow:
- Cisco IOS-XE best practices
- RFC-compliant MPLS implementations
- Industry-standard naming conventions
- Production-ready verification steps

## Limitations

- Configurations are templates - adapt to your specific environment
- IPv4 only (IPv6 support planned)
- Assumes MPLS core is already configured with LDP/RSVP
- No automatic commit to devices (intentional - human review required)

## Support & Feedback

This is a free tool for the network engineering community. While there's no official support:
- Test configurations in lab before production use
- Verify commands match your IOS version
- Review all generated configs before deployment

## Version

Current Version: **2.0**

**Recent Updates:**
- Added dual-tunnel MPLS-TE support
- Interactive network topology diagrams
- Python script generators matching web interface
- Enhanced VRF analyzer with traffic flow visualization
- Improved configuration validation

## License

This software is proprietary and licensed for specific use cases only. See the [LICENSE.txt](LICENSE.txt) file for complete terms and conditions.

**Permitted Uses:**
- Internal organizational use for network configuration generation
- Educational and training purposes
- Laboratory and testing environments
- Configuration generation for your own networks

**Restrictions:**
- No redistribution or resale
- No commercial service offerings using this tool
- No incorporation into products for redistribution
- No modification or reverse engineering

For commercial licensing inquiries, please contact the copyright holder.

---

**Built for network engineers, by network engineers.**

*Generate accurate MPLS configurations in minutes, not hours.*
