# Contributing a Vehicle

Thank you for helping make emergency response data available for more EVs!

## Before You Start

**Check if the vehicle is already supported or in progress:**

<details>
<summary>Currently supported vehicles (78 models)</summary>

| Make | Models |
|------|--------|
| Acura | ZDX |
| Audi | e-tron, e-tron GT, Q4 e-tron, Q6 e-tron, Q8 e-tron |
| BMW | i4, i5, i7, iX |
| Cadillac | Celestiq, Escalade IQ, Lyriq, Optiq |
| Chevrolet | Blazer EV, Bolt, Equinox EV, Silverado EV |
| Dodge | Charger Daytona 2dr, Charger Daytona 4dr |
| Ford | E-Transit, F-150 Lightning, Mustang Mach-E |
| Genesis | G80 EV, GV60, GV70 EV |
| GMC | Hummer EV Pickup, Hummer EV SUV, Sierra EV |
| Honda | Prologue |
| Hyundai | Ioniq 5, Ioniq 5 N, Ioniq 6, Ioniq 9, Ioniq Electric, Kona Electric |
| Jeep | Wagoneer S |
| Kia | EV6, EV9, Niro EV |
| Lexus | RZ 450e |
| Lucid | Air, Gravity |
| Mazda | MX-30 |
| Mercedes | EQE, EQS SUV, G 580 E |
| Mini | Countryman SE |
| Nissan | Ariya, Leaf |
| Polestar | 2, 3, 4 |
| Porsche | Cayenne E-Hybrid, Macan Electric, Taycan |
| Ram | ProMaster EV |
| Rivian | Delivery Van, R1S, R1T |
| Rolls-Royce | Spectre |
| Subaru | Solterra |
| Tesla | Cybertruck, Model 3, Model S, Model X, Model Y, Roadster, Semi |
| Toyota | bZ, bZ4X, C-HR EV |
| Volkswagen | Golf GTE, ID.4, ID. Buzz |
| Volvo | EC40, EX30, EX40, EX90 |

</details>

Also check [open pull requests](../../pulls) to see if someone is already working on a vehicle.

## What to Submit

### Required

- **Rescue sheet PDF** — the official OEM emergency response guide or rescue sheet
  - Must be from a publicly available source (OEM website, Euro NCAP, NFPA, etc.)
  - Rescue sheets (2-4 pages, structured) are preferred over full ERGs (50+ pages)
  - Must be the **English** version

- **metadata.yaml** — basic vehicle information (see template below)

### Where to Find Rescue Sheets

- [Euro NCAP Rescue Sheets](https://www.euroncap.com/en/vehicle-safety/rescue-sheets/) — large free database
- [NFPA Emergency Field Guide](https://www.nfpa.org/training-and-events/by-topic/alternative-fuel-vehicle-safety-training/emergency-field-guide) — US-focused
- OEM websites — many manufacturers publish rescue sheets directly
- [Moditech Rescue Sheets](https://www.moditech.com/) — industry standard (check for free access)

## How to Submit

### 1. Fork & Clone

Fork this repository and clone it locally.

### 2. Create a Vehicle Directory

Copy the template:

```bash
cp -r submissions/_template submissions/MAKE_MODEL
```

Use UPPERCASE with underscores. Examples:
- `BYD_SEAL`
- `FIAT_500E`
- `XIAOMI_SU7`
- `HYUNDAI_IONIQ_7`

### 3. Add the Rescue Sheet PDF

Place the PDF in your vehicle directory. Name it descriptively:

```
submissions/BYD_SEAL/BYD_Seal_Rescue_Sheet.pdf
```

### 4. Fill in metadata.yaml

```yaml
make: "BYD"
model: "Seal"
year_range: "2023-2025"       # Model years covered by this rescue sheet
source_url: "https://..."     # Where you downloaded the PDF
source_type: "rescue_sheet"   # rescue_sheet | erg | other
language: "en"
submitter_notes: ""           # Optional: anything we should know
```

### 5. Open a Pull Request

Push your branch and open a PR. The PR template will guide you through a checklist.

## Review Process

Every submission is manually reviewed. We check:

1. **Source legitimacy** — is this an official OEM document?
2. **Content quality** — are diagrams legible? Is the document complete?
3. **Correct vehicle match** — does the PDF match the claimed make/model?
4. **No duplicates** — is this vehicle already covered?

Reviews typically take a few days. We may ask questions or request a different source document.

## What Happens After Approval

Once approved, we:
1. Process the PDF through our knowledge base pipeline
2. Verify extracted data against the source document
3. Publish the vehicle to the app's remote asset server
4. The vehicle becomes available to all app users automatically

## Guidelines

- **One vehicle per PR** — makes review easier
- **Don't modify other vehicles' submissions** — open a separate issue
- **English documents only** for now
- **No scanned/photographed documents** — we need proper PDFs with selectable text
- **Don't submit documents behind paywalls** — only publicly accessible sources
