
### To verify
Copy the file content and paste on the [univerifier](https://univerifier.io/) then click verify. The credential will verify and show expired as this tenure is expired.

### To issue credentials
A VC service is hosted at `https://ipsweb.vc.opsec.id/titles/{titleNo}`.
To request a VC of an existing title, append the title No you are interested in.
Visit [https://a100.gov.bc.ca/pub/ipsweb](https://a100.gov.bc.ca/pub/ipsweb) to browse available titles.

### To inspect dids
[Click here](https://dev.uniresolver.io/#did:web:ipsweb.vc.opsec.id) and click resolve to resolve the web did
[Click here](https://dev.uniresolver.io/#did:indy:bcovrin:test:HnJJkDxeebDyLqyZxxxRfK) and click resolve to resolve the linked indy did

### Features
- EdDSA NIST approved signature algorithm
- StatusList2021 revocation management
- Linked indy did
- Validity proof

### Tenure 745 VC
```json-ld
{
  "@context": [
    "https://www.w3.org/2018/credentials/v1",
    "https://w3id.org/vc/status-list/2021/v1",
    "https://w3id.org/traceability/v1",
    {
      "@vocab": "urn:bcgov:attributes#"
    }
  ],
  "id": "https://ipsweb.vc.opsec.id/titles/745",
  "type": [
    "VerifiableCredential",
    "BCGovTenureCredential"
  ],
  "issuer": {
    "id": "did:web:ipsweb.vc.opsec.id",
    "description": "Demo issuer to issue public titles held by PROVINCE OF BRITISH COLUMBIA MINISTRY OF ENERGY, MINES AND LOW CARBON INNOVATION INTEGRATED PETROLEUM SYSTEM in a Verifiable Credential format"
  },
  "issuanceDate": "1958-07-29T00:00:00Z",
  "expirationDate": "1979-07-29T00:00:00Z",
  "credentialSubject": {
    "type": [
      "BCGovTenure"
    ],
    "tracts": [
      {
        "type": [
          "BCGovTenureTract"
        ],
        "numbers": [
          "NTS 094-B-08 BLK I UNITS 92 93",
          "NTS 094-B-09 BLK A UNITS 2 3"
        ],
        "inclusions": "PETROLEUM AND NATURAL GAS DOWN TO BASE OF 32505 BELLOY ZONE",
        "exclusions": "NATURAL GAS IN 34002 ARTEX-HALFWAY-DOIG ZONE",
        "notes": "32505 BELLOY ZONE DEFINED IN THE INTERVAL 6537'-6626' MD ON THE GAMMA RAY-NEUTRON LOG OF THE WELL W.A. 141 d-94-I/94-B-8 34002 ARTEX-HALFWAY-DOIG ZONE DEFINED IN THE INTERVAL 5970.7'-6952.7' ON THE GAMMA RAY NEUTRON LOG OF THE WELL W.A. 238 C-53-D/94-B-09"
      }
    ],
    "caveats": [],
    "ownership": [
      {
        "companyName": "PACIFIC CANBRIAM ENERGY LIMITED",
        "interestPercent": 100
      }
    ],
    "area": "286"
  },
  "credentialStatus": {
    "type": "StatusList2021Entry",
    "id": "https://ipsweb.vc.opsec.id/status-list#745",
    "statusPurpose": "revocation",
    "statusListCredential": "https://ipsweb.vc.opsec.id/status-list",
    "statusListIndex": "745"
  },
  "proof": {
    "type": "Ed25519Signature2018",
    "proofPurpose": "assertionMethod",
    "verificationMethod": "did:web:ipsweb.vc.opsec.id#verkey",
    "created": "2024-03-04T01:24:20+00:00",
    "jws": "eyJhbGciOiAiRWREU0EiLCAiYjY0IjogZmFsc2UsICJjcml0IjogWyJiNjQiXX0..A_mqqGMgYjuHmxDLL3xScMN8MftZvxSNxHzgbVPYVlKaxsp4hYouLSqzhfHs7JtlJLspuic9tqNo7KfO8pGfDw"
  },
  "validFrom": "1958-07-29T00:00:00Z"
}
```
