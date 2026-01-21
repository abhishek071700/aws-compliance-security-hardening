# Lambda → VPC Migration (Reference Notes)

## Goals
- network segmentation
- outbound traffic governance

## Notes
- deploy into private subnets
- use VPC endpoints to reduce NAT
- consider cold start impact due to ENI
