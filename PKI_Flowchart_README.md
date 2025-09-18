# PKI Signature and Verification Flowchart

This flowchart illustrates the complete process of PKI (Public Key Infrastructure) signature creation and verification.

## Files Included

- `pki_flowchart.dot` - Source file in DOT (Graphviz) format
- `pki_flowchart.png` - Rendered flowchart in PNG format
- `pki_flowchart.svg` - Rendered flowchart in SVG format (scalable)
- `PKI_Flowchart_README.md` - This documentation file

## Process Overview

### PKI Signing Process
1. **Input Data**: Original data that needs to be signed
2. **Hashing**: Apply a hash algorithm (e.g., SHA-256) to the data, producing a hash value
3. **Private Key Usage**: Use the signer's private key to encrypt the hash value, generating a digital signature
4. **Output**: Send the original data and the digital signature to the recipient

### PKI Verification Process
1. **Input Data**: Receive the original data and the digital signature
2. **Hashing**: Apply the same hash algorithm to the received data, producing a hash value
3. **Public Key Usage**: Use the signer's public key to decrypt the digital signature, retrieving the hash value
4. **Comparison**: Compare the decrypted hash value with the recalculated hash value
   - **If they match**: The data is authentic and untampered
   - **If they do not match**: The data may have been tampered with or the signature is invalid

## Flowchart Features

- **Clear Visual Separation**: Signing and verification processes are in separate colored sections
- **Appropriate Symbols**: 
  - Rectangles for data/input/output
  - Ellipses for processes
  - Diamond for decision points
  - Different colors to distinguish between types of operations
- **Legend**: Included to explain the symbol meanings
- **Flow Indicators**: Arrows show the direction of data flow
- **Decision Outcomes**: Clear labeling of match/no match results

## Usage

To view the flowchart:
- Open `pki_flowchart.png` for a standard image view
- Open `pki_flowchart.svg` in a web browser for a scalable vector view
- Use the `pki_flowchart.dot` file with Graphviz tools for editing

To regenerate the images from the DOT source:
```bash
dot -Tpng pki_flowchart.dot -o pki_flowchart.png
dot -Tsvg pki_flowchart.dot -o pki_flowchart.svg
```

## Security Concepts Illustrated

- **Digital Signatures**: Demonstrates how private keys create signatures
- **Signature Verification**: Shows how public keys verify signatures
- **Hash Functions**: Illustrates the role of cryptographic hashing
- **Data Integrity**: Visual representation of how tampering is detected
- **Authentication**: Shows how the signature proves data origin