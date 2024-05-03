# Vocabulary

This page outlines the vocabulary present in the BC Tenure Title Verifiable Credential as well as an example.

## BCTenureTitle

Tenure agreements with the Province give private developers rights to petroleum and natural gas resources. Typically, agreements are for three to ten years and can be renewed or extended, require exploration or development, and call for payment of rents and royalties to the Province.  Rights are provided to specific areas and may include rights to all depths, or may be restricted to certain geological formations. 

## PetroleumAndNaturalGasLease

## PetroleumLease

## NaturalGasLease

## NaturalGasLicence

## DrillingLicence

## DrillingReservation

## StorageLease

## Parcel

## term

This describes the length of time (term) granted for each title, expressed in YYYY. This date does not change.

## area

This attribute is the surface area in planned use, measured in hectares. This includes 3 dimensional layers.

## titleType

This field specifies the type of title based on the PNG Act. Title types can include the following: 1. Lease (Part 6); 2. Permit (Part 5); 3. Drilling Licence (Part 5.1), and 4. Storage Reservoir Licence (Part 14.130). Each title has only one title type.

## titleNumber

A number is used to uniquely identify a title, assigned based on administrative policy by the TRSB. The title number is associated with the Exploration Licence outlined in [Section 126, part 14.126 of the PNG Act](https://www.bclaws.gov.bc.ca/civix/document/id/complete/statreg/96361_01#section126)

## originType

This field specifies the type of title origin based on the PNG Act. Each title origin has only one title origin type.

## originNumber

A number is used to uniquely identify a title origin, assigned based on administrative policy by the TRSB. The title origin number is associated with the Exploration Licence outlined in [Section 126, part 14.126 of the PNG Act](https://www.bclaws.gov.bc.ca/civix/document/id/complete/statreg/96361_01#section126)

## titleHolders

The PNG Act describes a "holder of a location" as meaning "in accordance with the context, a permittee, licensee" . In this credential, the term title holder is used to reference a person in whose name a PNG title document is recorded in the division records.

## holderName

Title holders can be registered companies, and/or persons. Lessee is defined by the PNG Act as "a person in whose name a lease is recorded in the division records".

## holderInterest

A Title Holder will hold a percentage (%) interest in the title. Percent interest defines the percentage of interest allotted to each party named in the PNG title document. Percentage of ownership can be divided up to eight digits and should always equal 100% total.

## tracts

A Tract is an area of land within a title defined by locations sharing identical rights. This attribute has all of the tract(s) information contained within a title.

## tractLocations

Tract Location outlines the precise location for a tract listed on a PNG title document using specific attributes from one of two land survey systems currently in use within BC.

## tractRights

Tract Rights are defined as either "Included (I)" or "Excluded (E)". Zone names are coded "Petroleum (P)" "Petroleum Natural Gas (PNG)" (or other relevant codes). Each right will be denoted by its corresponding letter. This section outlines the rights associated with each individual tract listed on a PNG title document. This would be linked with a BC business number (i.e. BC123456). Tract rights are identified using specific Code Lists. There are Stratigraphic Codes (used to define tract rights) and Standard Zone Designations.

## rightLocations

## tractNotes

Tract Notes outlines specific notes or points associated with each tract. Definitions of zones used in tract rights reference specific depth intervals in the type well named in the same note. These are used to describe the type wells and the intervals in the type wells that are used to create the type.

## caveats

Caveats provide information and guidance to the tenure holder that will assist in activity planning by identifying potential access restrictions. Caveats will also flag concerns identified through pre-tenure consultation and may recommend engagement with First Nations, stakeholders, and other agencies as appropriate. Caveats often point to relevant statute and policy and are not binding or enforced by the Ministry.

## wells

Wells are identified by their authorization numbers.


# Example
```json
{
    "@context": [
        "https://www.w3.org/ns/credentials/v2"
    ],
    "type": [
        "VerifiableCredential"
    ],
    "issuer": {
        "type": [
            "GovernmentOrganization"
          ],
        "id": "did:web:orgbook.vonx.io:issuer:DirectorOfPetroliumLand",
        "name": "Governement of British Columbia",
        "employee": {
            "type": [
              "Person"
            ],
            "jobTitle": "Director of Petrolium Land",
            "description": "An officer or employee of the ministry who is designated as the Director of Petroleum Lands by the minister."
          },
        "image": "https://orgbook.gov.bc.ca/img/icons/apple-touch-icon-152x152.png"
    },
    "validFrom": "2010-01-01T19:23:24Z",
    "validUntil": "2020-01-01T19:23:24Z",
    "credentialSubject": {
        "type": ["BCTenureTitle"],
        "legalAct": [
            "https://www.bclaws.gov.bc.ca/civix/document/id/complete/statreg/96361_01",
            "https://www.bclaws.gov.bc.ca/civix/document/id/complete/statreg/10_82"
            ],
        "term": "5",
        "area": "1056",
        "originType": "PetroliumAndNaturalGasLease",
        "originNumber": "61689",
        "titleType": "PetroliumAndNaturalGasLease",
        "titleNumber": "64786",
        "titleHolders": [
            {
                "type": ["Organization"],
                "id": "https://orgbook.gov.bc.ca/entity/A0131571",
                "url": "https://orgbook.gov.bc.ca/entity/A0131571",
                "holderName": "PACIFIC CANBRIAM ENERGY LIMITED",
                "holderInterest": "80.00000000"
            },
            {
                "type": ["Organization"],
                "id": "https://orgbook.gov.bc.ca/entity/A0086333",
                "url": "https://orgbook.gov.bc.ca/entity/A0086333",
                "holderName": "CANADIAN SPIRIT RESOURCES INC.",
                "holderInterest": "20.00000000"
            }
        ],
        "tracts": [
            {
                "tractLocations": [
                    "TWP 083 RGE 25 SEC 10 15"
                ],
                "tractRights": [
                    {
                        "type": "PETROLEUM AND NATURAL GAS",
                        "included": true,
                        "rightLocations": [
                            "IN 34011 ARTEX-HALFWAY-DOIG ZONE",
                            "IN 33018 MONTNEY (EXCLUDING BASAL LAG) ZONE"
                        ]
                    }
                ],
                "tractNotes": [
                    "34011 ARTEX-HALFWAY-DOIG (BASE 'A' MARKER TO BASE DOIG PHOSPHATE) ZONE IDENTIFIED IN THE INTERVAL 1674.5M-1944.7M ON THE PHOTO-DENSITY DUAL SPACED NEUTRON LOG AND THE ARRAY INDUCTION LOG OF THE WELL W.A. 24456 1-28-81-20 W6M",
                    "33018 MONTNEY (EXCLUDING BASAL LAG) ZONE DEFINED IN THE INTERVAL 1944.7M-2217.6M ON THE PHOTO-DENSITY DUAL SPACED NEUTRON LOG AND THE ARRAY INDUCTION LOG OF THE WELL W.A. 24456 1-28-81-20 W6M"
                ]
            },
            {
                "tractLocations": [
                    "TWP 083 RGE 25 SEC 11 14"
                ],
                "tractRights": [
                    {
                        "type": "PETROLEUM AND NATURAL GAS",
                        "included": true,
                        "rightLocations": [
                            "IN 33018 MONTNEY (EXCLUDING BASAL LAG) ZONE"
                        ]
                    }
                ],
                "tractNotes": [
                    "33018 MONTNEY (EXCLUDING BASAL LAG) ZONE DEFINED IN THE INTERVAL 1944.7M-2217.6M ON THE PHOTO-DENSITY DUAL SPACED NEUTRON LOG AND THE ARRAY INDUCTION LOG OF THE WELL W.A. 24456 1-28-81-20 W6M"
                ]
            }
        ],
        "wells": [],
        "caveats": [
            "PARCEL LOCATED WITHIN TREATY 8. CONSULTATION MAY BE REQUESTED BY A TREATY 8 FIRST NATION."
        ]
    }
}
```
