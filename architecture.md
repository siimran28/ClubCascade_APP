# ClubCascade - Architecture Document

## App Overview
ClubCascade is an event management and engagement platform for college students and organizers, solving miscommunication and scattered updates through a centralized digital platform.

## Core MVP Features
1. **Event Discovery**: Browse upcoming, ongoing, and past events with search/filter
2. **Dual User Roles**: Student view (explore, register) and Organizer view (create, manage events)
3. **Registration System**: One-tap registration with QR code generation for attendance
4. **AI Recommendations**: Smart event suggestions based on user interests and history
5. **Notifications**: Real-time updates for new events, changes, and reminders
6. **Analytics Dashboard**: Event statistics and engagement metrics for organizers

## Tech Stack
- **Frontend**: Flutter (cross-platform)
- **Storage**: Local storage with shared_preferences
- **State Management**: Built-in StatefulWidget
- **UI Design**: Custom university-inspired theme (blue, gold, white) with generous spacing

## File Structure

### Models (lib/models/)
1. `user.dart` - User data model (id, name, email, role, interests, attendance history)
2. `event.dart` - Event data model (id, title, description, date, venue, organizer, category, image, registrations)
3. `registration.dart` - Registration data model (id, userId, eventId, qrCode, checkInStatus)

### Services (lib/services/)
1. `user_service.dart` - User operations and authentication simulation
2. `event_service.dart` - Event CRUD operations with sample data
3. `registration_service.dart` - Registration and QR code management
4. `recommendation_service.dart` - AI-powered event recommendations based on interests
5. `storage_service.dart` - Local storage wrapper for persistence

### Screens (lib/screens/)
1. `splash_screen.dart` - ClubCascade branding with tagline
2. `auth_screen.dart` - Login/signup with college email
3. `home_screen.dart` - Main dashboard with navigation (events, profile, analytics for organizers)
4. `events_list_screen.dart` - Browse all events with search and filters
5. `event_detail_screen.dart` - Full event information with registration button
6. `create_event_screen.dart` - Organizers create/edit events
7. `my_events_screen.dart` - User's registered events with QR codes
8. `profile_screen.dart` - User profile with interests and settings
9. `analytics_screen.dart` - Organizer dashboard with event statistics

### Widgets (lib/widgets/)
1. `event_card.dart` - Reusable event list item
2. `qr_code_widget.dart` - QR code display for event pass
3. `filter_chip_row.dart` - Category/department filters
4. `stat_card.dart` - Analytics metric display

## Implementation Steps
1. Setup dependencies (qr_flutter, shared_preferences, intl)
2. Update theme with university colors (royal blue, gold, white)
3. Create data models with toJson/fromJson/copyWith
4. Implement service classes with sample data in local storage
5. Build splash screen with branding
6. Create authentication flow (student/organizer role selection)
7. Implement home screen with bottom navigation
8. Build events list with search and filters
9. Create event detail screen with registration functionality
10. Implement QR code generation for registrations
11. Build create event screen for organizers
12. Create my events screen showing user registrations
13. Implement AI recommendation service
14. Build analytics dashboard for organizers
15. Add profile screen with interest selection
16. Test and debug with compile_project

## Design Guidelines
- University-inspired color palette: Royal Blue (#1E3A8A), Gold (#F59E0B), White (#FFFFFF)
- Generous spacing (24-32px between sections)
- Elegant typography with Inter font family
- Smooth animations and transitions
- Clean dashboard-style cards with elevation
- Custom styled buttons avoiding Material defaults
