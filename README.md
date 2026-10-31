# FrameQuote

Custom Frame Price Calculator & Order Tracker — Semester Project for **Web Technologies (CS-102)**, GU-Tech (Al Ghazali University).

FrameQuote helps wholesale buyers and shop customers get an instant price for a custom frame and place an order: enter the artwork size, choose a border and glass type, see a calculated estimate, submit the request, and track its status until delivery.

## Team

| Name | Roll No. | Role |
|------|----------|------|
| Syed Hashir Ali | 2622-4CS-026 | Developer |
| Ibadullah | 2622-4CS-028 | Partner |

## Project proposal

See [docs/FrameQuote_Semester_Project_Proposal.pdf](docs/FrameQuote_Semester_Project_Proposal.pdf).

## Planned features

1. View frame options (border styles, glass types, rates)
2. Enter artwork size (width × height, inches)
3. Choose options (border, glass, quantity)
4. Instant price estimate
5. Submit order request (name, phone, notes)
6. Get an order ID
7. Track order status (order ID + phone)
8. Admin login and order list
9. Update order status (Received → In production → Ready → Delivered)
10. Manage options and prices

**MVP:** price calculator (2–4), order submission (5–6), admin order list with status update (8–9).

Price formula: `price = (area × glass rate + perimeter × border rate) × quantity`

## Architecture

| Part | Responsibility |
|------|----------------|
| Frontend | Calculator, order form, status page, admin page — HTML, CSS, JavaScript |
| Backend | Validation, price formula, order IDs, admin login, status updates |
| Database | Border styles, glass types, orders, status history (hosted database) |

## Git workflow

- `main` is always working code; no direct pushes for features.
- Each feature is built on its own branch (`feature/<name>`) and merged through a pull request reviewed by the partner.
- Small commits with clear messages.
- Secrets live in environment variables (`.env`), never in the repository.
