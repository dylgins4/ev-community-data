# Smart EV Emergency Response Guide — Community Vehicle Data

Community-contributed emergency response data for electric vehicles, used by the [Smart EV Emergency Response Guide](https://play.google.com/store/apps/details?id=com.example.ev_mobile) app.

This app helps first responders quickly access high-voltage safety, extrication, fire response, and other emergency procedures for electric vehicles.

## How It Works

1. **You submit** a vehicle's rescue sheet PDF + metadata via pull request
2. **We review** the submission for accuracy, source legitimacy, and content quality
3. **Once approved**, the vehicle data is processed and published to the app

All submissions are manually reviewed before they appear in the app. This is emergency response content — accuracy is critical.

## What We Need

We're looking for **OEM rescue sheets** (also called Emergency Response Guides) for EV models not yet in the app. These are published by manufacturers and typically include:

- Vehicle identification and recognition
- High-voltage component locations
- Cut zones and structural diagrams
- High-voltage disable procedures
- Fire response procedures
- Towing guidelines

## Currently Supported Vehicles

Tesla, Rivian, Ford, Chevrolet, Hyundai, Nissan, Volkswagen, Volvo, Kia, BMW, Porsche, Audi, Mercedes, Cadillac, GMC, Genesis, Polestar, Lucid, Toyota, Lexus, Honda, Subaru, Jeep, Dodge, Mini, Mazda, Rolls-Royce, Acura, Ram — 78 models total.

See [CONTRIBUTING.md](CONTRIBUTING.md) for the full list and how to submit new vehicles.

## Quick Start

1. Fork this repo
2. Copy `submissions/_template/` to `submissions/MAKE_MODEL/` (e.g., `submissions/BYD_SEAL/`)
3. Add the rescue sheet PDF and fill in `metadata.yaml`
4. Open a pull request

See [CONTRIBUTING.md](CONTRIBUTING.md) for detailed instructions.

## License

Submitted rescue sheet PDFs remain the intellectual property of their respective manufacturers. This repository organizes publicly available safety documents for use in emergency response applications.
