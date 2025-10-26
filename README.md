# TicketFlow - Modern Ticket Management System

A modern, responsive ticket management system built with Next.js, React, and TypeScript. TicketFlow helps teams streamline their workflow, improve collaboration, and boost productivity by providing an intuitive interface for managing support tickets.

## Features

- **Landing Page**: Professional landing page with hero section, features showcase, and call-to-action
- **Authentication**: Secure login and signup system with form validation
- **Dashboard**: Real-time statistics and analytics with interactive charts
  - Total tickets overview
  - Open, in-progress, and closed ticket counts
  - Weekly activity charts (line, bar, and pie charts)
  - Visual status distribution
- **Ticket Management**: Full CRUD operations for tickets
  - Create new tickets with title, description, and priority
  - Edit existing tickets and update status
  - Delete tickets with confirmation
  - Filter tickets by status (Open, In Progress, Closed)
  - Priority levels (Low, Medium, High)
- **Responsive Design**: Fully responsive layout that works on mobile, tablet, and desktop
- **Modern UI**: Clean, professional design with dark mode support
- **Local Storage**: Persistent data storage using browser localStorage

## Tech Stack

- **Framework**: Next.js 16 with App Router
- **Language**: TypeScript
- **Styling**: Tailwind CSS v4
- **UI Components**: shadcn/ui
- **Charts**: Recharts
- **State Management**: React Hooks
- **Storage**: Browser localStorage

## Getting Started

### Prerequisites

- Node.js 18+ or higher
- npm or yarn package manager

### Installation

1. **Clone or download the project**
   \`\`\`bash
   git clone <repository-url>
   cd ticketflow
   \`\`\`

2. **Install dependencies**
   \`\`\`bash
   npm install
   # or
   yarn install
   \`\`\`

3. **Run the development server**
   \`\`\`bash
   npm run dev
   # or
   yarn dev
   \`\`\`

4. **Open your browser**
   Navigate to [http://localhost:3000](http://localhost:3000)

## Usage

### Landing Page

Visit the home page to see the TicketFlow landing page with:
- Hero section with call-to-action buttons
- Features showcase
- Navigation to login/signup

### Authentication

1. **Sign Up**: Create a new account with your name, email, and password
   - Password must be at least 6 characters
   - Passwords must match
   - Email validation is performed

2. **Login**: Sign in with your email and password
   - Form validation ensures all fields are filled
   - Email format is validated

### Dashboard

After logging in, you'll see the dashboard with:
- **Statistics Cards**: Overview of total, open, in-progress, and resolved tickets
- **Charts**: Visual representation of ticket trends and status distribution
- **Navigation**: Sidebar menu to access different sections

### Ticket Management

1. **View Tickets**: Navigate to the Tickets section to see all tickets
2. **Create Ticket**: Click "Create Ticket" button to open the creation modal
   - Enter title (required)
   - Add description (optional)
   - Select priority level
   - Ticket is created with "Open" status by default

3. **Edit Ticket**: Click "Edit" on any ticket to modify it
   - Update title, description, status, and priority
   - Changes are saved immediately

4. **Delete Ticket**: Click "Delete" to remove a ticket
   - Confirmation dialog prevents accidental deletion

5. **Filter Tickets**: Use filter buttons to view tickets by status
   - All: Show all tickets
   - Open: Show only open tickets
   - In Progress: Show tickets being worked on
   - Closed: Show resolved tickets

## Project Structure

\`\`\`
ticketflow/
├── app/
│   ├── layout.tsx              # Root layout
│   ├── globals.css             # Global styles and design tokens
│   ├── page.tsx                # Landing page
│   ├── auth/
│   │   ├── layout.tsx          # Auth layout
│   │   ├── login/
│   │   │   └── page.tsx        # Login page
│   │   └── signup/
│   │       └── page.tsx        # Signup page
│   └── dashboard/
│       ├── layout.tsx          # Dashboard layout with sidebar
│       ├── page.tsx            # Dashboard home
│       └── tickets/
│           └── page.tsx        # Tickets management page
├── components/
│   ├── ui/                     # shadcn/ui components
│   ├── auth/
│   │   ├── login-form.tsx      # Login form component
│   │   └── signup-form.tsx     # Signup form component
│   └── tickets/
│       ├── ticket-list.tsx     # Ticket list display
│       ├── create-ticket-modal.tsx  # Create ticket modal
│       └── edit-ticket-modal.tsx    # Edit ticket modal
├── hooks/                      # Custom React hooks
├── lib/                        # Utility functions
├── public/                     # Static assets
└── package.json               # Project dependencies
\`\`\`

## Data Storage

The application uses browser localStorage to persist data:

- **User Data**: Stored when user logs in/signs up
  \`\`\`json
  {
    "id": "unique-id",
    "name": "User Name",
    "email": "user@example.com"
  }
  \`\`\`

- **Tickets**: Stored as an array of ticket objects
  \`\`\`json
  {
    "id": "ticket-id",
    "title": "Ticket Title",
    "description": "Ticket Description",
    "status": "open|in-progress|closed",
    "priority": "low|medium|high",
    "createdAt": "ISO-8601-timestamp",
    "updatedAt": "ISO-8601-timestamp"
  }
  \`\`\`

## Features in Detail

### Authentication System

- Email and password validation
- Secure password confirmation
- User session management
- Automatic redirect to login for unauthenticated users
- Logout functionality

### Dashboard Analytics

- Real-time ticket statistics
- Interactive charts showing:
  - Tickets created vs resolved over time
  - Weekly activity breakdown
  - Status distribution pie chart
- Responsive chart layouts for all screen sizes

### Ticket Management

- **Status Tracking**: Open, In Progress, Closed
- **Priority Levels**: Low, Medium, High
- **Filtering**: Quick filter by status
- **Search**: View all tickets or filtered results
- **Timestamps**: Track creation and update times

### Responsive Design

- Mobile-first approach
- Collapsible sidebar navigation
- Responsive grid layouts
- Touch-friendly buttons and inputs
- Optimized modals for small screens
- Adaptive typography and spacing

## Customization

### Styling

The app uses Tailwind CSS v4 with design tokens defined in `app/globals.css`. To customize colors:

1. Edit the CSS variables in `app/globals.css`
2. Update the color tokens (primary, secondary, accent, etc.)
3. Changes apply globally throughout the app

### Adding New Features

1. **New Pages**: Create new route folders in `app/` directory
2. **New Components**: Add components to `components/` directory
3. **New Hooks**: Create custom hooks in `hooks/` directory
4. **Styling**: Use Tailwind classes and design tokens

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## Performance

- Optimized React components with proper memoization
- Efficient state management with React Hooks
- Responsive images and lazy loading
- Minimal bundle size with tree-shaking

## Accessibility

- Semantic HTML elements
- ARIA labels and roles
- Keyboard navigation support
- Color contrast compliance
- Screen reader friendly

## Deployment

### Deploy to Vercel

1. Push your code to GitHub
2. Connect your repository to Vercel
3. Vercel automatically deploys on push
4. Your app is live at `your-project.vercel.app`

### Deploy to Other Platforms

The app can be deployed to any platform that supports Next.js:
- Netlify
- AWS Amplify
- DigitalOcean
- Heroku
- Self-hosted servers

## Development

### Available Scripts

\`\`\`bash
# Start development server
npm run dev

# Build for production
npm run build

# Start production server
npm start

# Run linting
npm run lint
\`\`\`

## Troubleshooting

### Data Not Persisting

- Check browser localStorage is enabled
- Clear browser cache and try again
- Check browser console for errors

### Login Issues

- Ensure email format is valid
- Password must be at least 6 characters
- Check that localStorage is not full

### Charts Not Displaying

- Ensure JavaScript is enabled
- Check browser console for errors
- Try refreshing the page

## Future Enhancements

- Database integration (Supabase, Firebase)
- Real-time collaboration features
- Email notifications
- Advanced filtering and search
- User roles and permissions
- Ticket comments and attachments
- Export functionality
- API integration
- Mobile app

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is open source and available under the MIT License.

## Support

For support, please open an issue on the GitHub repository or contact the development team.

## Changelog

### Version 1.0.0 (Initial Release)

- Landing page with hero section
- Authentication system (login/signup)
- Dashboard with statistics and charts
- Complete ticket management (CRUD)
- Responsive design for all devices
- Dark mode support
- Local storage persistence

---

Built with ❤️ using Next.js and React
