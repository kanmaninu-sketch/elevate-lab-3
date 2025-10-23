# Elevate Lab 3 – AWS VPC Setup

## VPC Details
- **CIDR**: `10.0.0.0/24`
- **Region**: `ap-south-1` (Mumbai)
- **Availability Zone**: `ap-south-1b`

## Subnets
### Public Subnet – SUB11
- **CIDR**: `10.0.0.0/26`
- **Route Table**: RT11 (connected to Internet Gateway)

### Private Subnet – SUB22
- **CIDR**: `10.0.0.64/26`

#### CASE 1: No Internet
- **Route Table**: RTPRI (no NAT or Internet Gateway)

#### CASE 2: Internet via NAT Gateway
- **Route Table**: RTPRI (connected to NAT Gateway in SUB11)

## Summary
| Subnet | CIDR           | Internet Access      | Gateway Type     |
|--------|----------------|----------------------|------------------|
| SUB11  | `10.0.0.0/26`  |  Yes                 | Internet Gateway |
| SUB22  | `10.0.0.64/26` | NO-CASE1 / YES-CASE2 | NAT Gateway      |
****
