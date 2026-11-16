# OTP Verification UI

[![Live Demo](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-blue?style=for-the-badge&logo=github)](https://mrchandrayee.github.io/otp-verification-ui-1/)
[![HTML](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org) [![CSS](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org) [![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org)
[![License: MIT](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](./LICENSE)

Responsive, runnable OTP verification interface recreated from the uploaded 17.2-second screen recording.

## Video-matched UI
- Heading: `OTP Verification UI`
- Blue-to-purple radial gradient background
- Dark rounded verification card with blue outline/glow
- Purple lock icon tile
- Heading and helper text: “Enter the 6-digit verification code sent to your mobile number”
- Six individual OTP digit boxes
- Blue-to-purple `Verify OTP` button
- `Code expires in 00:59` countdown
- `Didn't receive the code? Resend OTP`
- Invalid OTP red alert and verified green success alert

## Interactions
- Auto-advance focus as digits are entered
- Backspace and arrow-key navigation
- Paste a full six-digit code
- Reject non-numeric input
- Countdown from 59 seconds; resend becomes available at expiry
- Invalid code displays an error
- Correct demo code displays success
- Resend clears the fields and restarts the timer

## Demo OTP
`123456`

The video shows an incorrect attempt followed by a successful verification. This project uses `123456` as a local demo code to reproduce those states.

## Run
Open `index.html` directly, or run:
```bash
python3 -m http.server 8000
```
Then visit http://localhost:8000.

## Source-derived CSS
The video visibly shows these declarations:
```css
.otp-box input:focus {
  transform: translateY(-6px) scale(1.05);
  border-color: #6ba3fa;
  background: rgba(59,130,246,0.12);
  box-shadow:
    0 0 0 4px rgba(96,165,250,0.15),
    0 0 25px rgba(96,165,250,0.45),
    inset 0 2px 6px rgba(255,255,255,0.08);
}

.otp-box::after {
  content: '';
  position: absolute;
  inset: -6px;
  border-radius: 22px;
  background: linear-gradient(135deg,#3b82f6,#8b5cf6);
  opacity: 0;
  filter: blur(12px);
  transition: 0.3s;
  z-index: -1;
}
```
The source screen recording does not expose the complete original HTML or JavaScript. The visible UI, text, CSS values and states are retained; the rest is implemented as a complete frontend reconstruction. No real SMS service, server-side OTP issuance, or authentication backend is connected.

## 👨‍💻 Author

**mrchandrayee** · [GitHub](https://github.com/mrchandrayee)

## 📄 License

[MIT License](./LICENSE)
