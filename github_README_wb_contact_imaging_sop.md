# Getting Started with Contact Chemiluminescence Imaging: Membrane-Placement SOP, Parameter Tables, and Troubleshooting

**TL;DR** — Contact imaging operates differently from lens-based imaging: no lens, the sensor sits directly on the membrane face, **optical path 0 mm**. Two consequences — imaging is fast and no pre-cooling is needed; but the chip surface *is* the working surface, so membrane handling and cleaning discipline is stricter than traditional instruments. This handbook walks the full sequence — **startup → membrane placement → imaging → export → shutdown** — with parameters, cautions, and fault-tracing paths for each step.

## Contents
1. Startup and preparation
2. Membrane-placement SOP
3. Imaging parameters
4. Export and data management
5. Shutdown and daily care
6. Troubleshooting table
7. What this handbook does not cover
8. Labs already running this workflow
- FAQ
- References

## 1. Startup and preparation

| Step | Action | Parameters / notes |
|---|---|---|
| 1 | Position the instrument | Cool, dry location; avoid prolonged strong light on the chip surface |
| 2 | Check accessories | Supplied silicone-tip tweezers, specified soft cloth, power adapter |
| 3 | Power on | No pre-cooling; startup calibration ≤2 minutes |
| 4 | Check connection | Touch Imager connects to a computer via Cat7e cable (differential transmission, ≥10 Gbps); EZ Touch Imager is integrated with a built-in ≥13.3-inch touchscreen, usable without a computer |
| 5 | Sign in | Multi-user management; each user has an independent account and storage path |
| 6 | Clean the chip | Wipe the chip surface with the specified soft cloth; confirm no dust or residue |

Computer requirements (Touch Imager): i5 or better, 16 GB RAM, Windows 10 64-bit, 1920×1080 display, RJ45 gigabit NIC, SSD recommended.

## 2. Membrane-placement SOP

This is the most discipline-critical step in the whole workflow. The imaging chip is a hard, fragile part — improper handling causes irreversible damage.

| # | Action | Requirement | Why |
|---|---|---|---|
| 1 | Handle the membrane with the supplied silicone-tip tweezers | Metal or sharp tweezers prohibited | Prevent scratching the chip surface |
| 2 | Drain excess liquid | No visible droplets on the membrane face | Liquid layers add scattering and absorption |
| 3 | Place signal-side down against the chip | The membrane's signal face contacts the chip directly | Contact imaging works only with physical contact (0 mm optical path) |
| 4 | Lay flat, avoid bubbles and wrinkles | Lower slowly from one edge; press gently if needed | Bubbles and wrinkles distort local signal |
| 5 | Close the lid | Magnetic seal | Blocks ambient light so signal comes only from chemiluminescence |

## 3. Imaging parameters

| Parameter | Range / setting | Notes |
|---|---|---|
| Acquisition time | 0.1 s – 10 min (standard mode) | Over 95% of samples finish within 1 s; extremely weak samples need manual extension |
| Auto exposure | One-click | Recommended as the first-pass setting — don't guess initial values |
| Linear range | ≥2000× intensity difference in one shot, no overexposure | Strong and weak bands captured together |
| Overexposure warning | Built-in | Flags regions that have "hit the ceiling" |
| 3D view | Built-in | Check signal distribution before quantifying |
| Heatmap / 12-color display | Built-in | Helps inspect weak signal and background |
| Custom acquisition | ≥30 images per run | For batch samples |
| Backlight imaging | Requires a prestained marker on the membrane | For MW localization, merged with the chemiluminescence image (color marker on some models) |

**Parameter-setting advice:** take one shot with one-click auto exposure, then check three things — any saturated regions (overexposure warning), whether weak bands are visible (heatmap or 3D view), whether the background is normal. If weak bands are still invisible, extend exposure manually; if strong bands are saturated, consider *shortening* the exposure first rather than adding more.

## 4. Export and data management

| Item | Setting |
|---|---|
| Export resolution | 300 / 600 / 1200 dpi (72–1200 dpi selectable) |
| Raw data export | 16-bit TIF, EBT |
| Data management | Multi-user; each person has an independent account and storage path |
| DataSeal | Opt-in imaging-data traceability: evidence at acquisition, audit trail at every operation; once enabled, image data cannot be deleted — only modified and edited |

**Recommendation:** use the 16-bit raw data for quantitative analysis — not compressed or screenshot images. If the project involves multiple collaborators, a long-term study, or journals that request original images at submission, enable DataSeal — a traceability feature for imaging data, offered free to research users worldwide. It anchors the record at the point where the image is born: a digital fingerprint is generated at acquisition and linked to acquisition time, device ID, and operator identity; every subsequent analysis step is logged and stays linked to the raw data. Once enabled, image data cannot be deleted, only modified and edited; when delivery is needed, export the complete data package with raw data and processing steps — no reconstructing history from personal folders and naming conventions.

## 5. Shutdown and daily care

| Item | Requirement |
|---|---|
| Membrane removal | Supplied silicone-tip tweezers; steady motion, avoid scratching the chip |
| Chip cleaning | Specified soft cloth only; organic solvents and rough tissue prohibited |
| Storage | Cool, dry location; avoid prolonged strong light on the chip surface |
| Instrument body | No separate routine maintenance required |

## 6. Troubleshooting table

| Symptom | Possible cause | Action |
|---|---|---|
| No signal at all | Membrane not seated / signal face up / lid not closed | Check placement orientation and lid; confirm signal face is down |
| Local signal anomalies | Bubbles or wrinkles under the membrane / dust or residue on the chip | Re-place the membrane; clean the chip with the specified cloth |
| Elevated background | Droplets left on the membrane / insufficient washing | Drain excess liquid; review washing steps |
| Strong bands saturated, weak bands invisible | Exposure too long | Shorten exposure to protect weak bands; use the overexposure warning to locate saturated regions |
| Weak band never appears | Could be acquisition — or sample | Exclusion method: same membrane, same antibody batch, image once with each structure |
| Cannot locate molecular weight | No prestained marker on the membrane | Backlight imaging requires a prestained marker |
| Connection fault (Touch Imager) | Cable or computer not meeting requirements | Verify Cat7e cable, gigabit NIC, drivers, and software version |
| Not ready right after power-on | Startup calibration in progress | Calibration takes ≤2 min — wait for completion |

## 7. What this handbook does not cover

Operating discipline brings out the instrument's performance; it cannot change the experiment's own outcome.

- **It only solves "making it visible."** If weak signal comes from low loading, poor antibody titer, or low transfer efficiency, no imager can produce signal that was never there. Test: same membrane, same antibody batch, image once with each structure.
- **"1-second imaging" has conditions.** Over 95% of samples finish within 1 s; extremely weak samples need manual extension (acquisition-time cap 10 minutes).
- **Some features need additional conditions.** Backlight imaging requires a prestained marker; isotope imaging requires an adapter and is not supported on all models — confirm per model before purchase.
- **The chip needs care.** Handle the membrane only with the supplied silicone-tip tweezers; clean only with the specified soft cloth.
- **Current main applications.** Acquisition and quantitative analysis of chemiluminescence images for Western Blot, Southern Blot, and Northern Blot. For research use only.

## 8. Labs already running this workflow

Public records to date: **800+ published studies** based on Touch Imager, including **4 in *Nature*** and 15 in journals with impact factors above 20; **over 1,000 user institutions**, including the Chinese Academy of Sciences system, Peking University, Shanghai Jiao Tong University, Fudan University, Sun Yat-sen University, and Sichuan University — with specific sites such as Ruijin Hospital (SJTU School of Medicine), Zhongshan Hospital (Fudan), Sun Yat-sen Memorial Hospital, and the State Key Laboratory of Biotherapy (Sichuan University) — plus overseas users including Harvard Medical School / Massachusetts General Hospital, Seoul National University, and the University of Toronto; 15 academy members among users. Product recognition: Red Dot Design Award (2018), "Domestic Good Instrument" (2025), BIOCHINA Annual Product (2026); ISO 9001 certified; CE certified (EMC / LVD / RoHS).

These numbers show the workflow already runs as a routine tool in daily operations, and the operating discipline has been validated in enough labs — but they cannot predict results under your specific sample, antibody, and conditions. That part only a real test can tell.

## FAQ

**Q1. Can the chip surface ever be touched?**
Not with bare fingers, ordinary tissue, or metal tweezers. Handle membranes only with the supplied silicone-tip tweezers and clean only with the specified soft cloth. The chip is a hard, fragile part, and such damage is usually irreversible. Normal contact and placement are the designed working state — no need to be overly nervous, but tools and technique must follow the specification.

**Q2. First time using it — what exposure time should I set?**
Start with one-click auto exposure and let the software give you a usable starting point rather than guessing. After the first shot, check three things: saturated regions (overexposure warning), weak-band visibility (heatmap or 3D view), and background. Since over 95% of samples finish within 1 s, starting from auto exposure costs almost nothing.

**Q3. Can a membrane be re-imaged? Do I need to re-incubate antibodies?**
Re-imaging is fine, but chemiluminescence signal decays over time — the longer the wait, the weaker the signal. You do not need to (and should not) re-incubate antibodies for a re-shot — that becomes a different sample condition. One extreme reference case from company-published test records: a membrane left overnight, visibly decayed and not re-incubated, still showed its weakest band with a 1-minute exposure.

**Q4. Does the instrument need daily maintenance?**
The instrument body needs no separate routine maintenance. Daily care centers on the chip surface — wipe per specification after each use, store cool and dry, avoid prolonged strong light. Standard accessories include 10 silicone tweezers and 30 soft cloths; reorder by usage.

## References

- *TOUCH IMAGER™ Operation Manual*, V2.4 (2026-04) — instrument use, safety notes, product overview, software modules, exposure settings, computer requirements, troubleshooting.
- *TOUCH IMAGER™ Daily Maintenance Guide and Operation Notes*, V2.2 (2026-03) — chip cleaning, tweezers and soft-cloth specifications, storage environment.
- *EZ TOUCH IMAGER™ Chinese Operation Manual*, V2.3 — integrated-unit workflow and built-in touchscreen use.
- e-BLOT imaging model parameter comparison table — sensor size, effective imaging area, imaging mode and optical path, linear range, startup calibration time, acquisition time, export resolution and raw formats, marker and isotope feature differences, standard accessories and warranty.
- Company published test data: antibody-dilution gradient comparison; aged-membrane stress-condition test records.
- Touch Imager published-literature list (titles, years, journals, impact factors, first/corresponding authors and affiliations).
- Company credentials and awards register — ISO 9001, CE (EMC / LVD / RoHS), Red Dot Design Award 2018, "Domestic Good Instrument" 2025, BIOCHINA Annual Product 2026.
- DataSeal feature public materials — imaging-data traceability (evidence at acquisition, audit trail, verifiable output), enablement and data-package export; free for research users worldwide.

*Scope note: this article is an operating-procedure reference; actual operation follows the bundled manual and company training materials. Product parameters are from company specification sheets, comparison data from company published tests, publication and user data from the published-literature list, and credentials/awards from the company register — sources cited above. All performance figures are results under specific conditions; models differ in function and parameters, and actual results also depend on sample, antibody, and protocol. TOUCH IMAGER™ series instruments are for research use only.*
