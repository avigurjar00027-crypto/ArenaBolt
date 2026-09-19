# ArenaBolt

**ArenaBolt by Thunder Developments** — a premium light-theme Free Fire esports tournament app.

## Confirmed payment model

ArenaBolt will use a **manual payment verification workflow**. No automatic payment gateway verification will be used in the initial version.

1. The administrator configures the UPI ID and QR code in the secure admin panel.
2. A user selects a coin package and opens the QR/UPI payment instructions.
3. The user pays externally using their UPI app.
4. The user submits the transaction ID and payment screenshot in the app.
5. The request appears as **Pending** in the admin panel.
6. An authorized admin approves or rejects the request.
7. Only after approval does the backend credit the user's wallet balance.
8. Every decision is recorded in an audit log, and rejected/duplicate requests cannot credit the wallet.

The backend—not the Android client—will enforce wallet balances, transaction status changes, duplicate transaction checks, admin authorization, and audit logging.

## Planned app scope

- Home, Tournaments, Events, Chats, and Friends navigation
- Solo, Duo, and Squad tournaments
- Email/password and guest login
- Friends chat and tournament chat
- Wallet, manual UPI submissions, redeem codes, and cash-prize controls
- In-app admin panel with server-side authorization
- Push notifications
- Force-update configuration
- Blue-purple premium mobile UI

## Security and compliance

Admin credentials and service credentials must remain server-side and out of the APK and repository. Configure them using deployment secrets/environment variables. Before enabling entry fees, cash prizes, withdrawals, or redeem codes, verify applicable laws, payment-provider rules, and Google Play policies for the target regions.
