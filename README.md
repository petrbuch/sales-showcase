# Mastercard Právní Pomoc - Web App

Lightweight web application for legal assistance form based on business requirements.

## Implementation Status ✅

Completed a 3-step form application matching the specifications from `input.md`:

### Step 1: Welcome Screen
- ✅ Mastercard branding with logo
- ✅ Main heading: "Potřebujete právní pomoc?"
- ✅ Subtitle about debt collection and document preparation
- ✅ Navigation: "O nás", "Služby", "Kontakt" 
- ✅ CTA button: "Nahlásit událost"
- ✅ Legal theme background with gavel motif

### Step 2: Card Verification
- ✅ Input field for exactly 8 digits
- ✅ Real-time validation (numbers only)
- ✅ Formatted input with space after 4 digits
- ✅ Placeholder: "např. 1234 5678"
- ✅ "Pokračovat" button (activated when valid)

### Step 3: Event Reporting Form
- ✅ Complete form with all required fields:
  - Name and surname *(required)*
  - Address *(required)*
  - Phone *(required)*
  - Email *(required)*
  - Description *(required, min 50 chars)*
  - Claimed amount *(required, min 1000 CZK)*
  - IČO *(optional for OSVČ)*
  - Debtor information *(optional)*
- ✅ File upload system:
  - Supports PDF, DOC, DOCX, PNG, JPG
  - Max 5 files, 10MB each
  - Drag & drop functionality
  - File validation and removal
- ✅ Form validation with Czech error messages
- ✅ Success confirmation message

## Technical Features

- **Authentic Mastercard Design**: Official color palette and branding
- **Responsive Design**: Works on desktop and mobile
- **Real-time Validation**: Immediate feedback on inputs
- **File Management**: Drag & drop with size/type validation
- **Czech Localization**: All text in Czech language
- **No Dependencies**: Pure HTML, CSS, JavaScript
- **Accessibility**: Proper form labels and error messages

## Design System

Updated to match official Mastercard branding:
- **Colors**: Primary Orange (#ff671b), Secondary Gold (#f38b00)
- **Typography**: Helvetica Neue with proper font weights
- **Logo**: Authentic overlapping circles design
- **Layout**: Clean, modern with proper spacing
- **Interactions**: Subtle hover effects matching brand guidelines

## Testing

🟢 **Server Status**: Running on http://localhost:8000

The application is currently live and accessible in your browser.

## Form Data Handling

Currently configured for demonstration:
- Form submission shows success message
- Data is logged to browser console
- No backend integration (as requested)

## Browser Compatibility

- Modern browsers (Chrome, Firefox, Safari, Edge)
- Mobile responsive design
- Progressive enhancement approach

## Development Notes

- Created: 2025-08-01
- Based on: `input.md` business requirements
- Design: Matches provided mockup images
- Language: Czech (as specified)
- No integrations: Frontend-only as requested

---

**Access the application**: http://localhost:8000