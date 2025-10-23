# Idealista Clone - Project Specifications

## 1. Product Overview

Idealista Clone is a comprehensive real estate marketplace platform that connects property buyers, sellers, and renters. The platform provides advanced search, listing management, user communication, and analytics features similar to the popular Spanish real estate portal Idealista.

**Primary Target Markets:** Spain and European real estate markets
**Primary Users:** Property owners, real estate agents, buyers, renters
**Platform Type:** Web and mobile-responsive real estate marketplace

### Key Vision
- Create a user-friendly platform for discovering and listing properties
- Provide professional tools for real estate agents and property owners
- Deliver accurate property valuations and market insights
- Enable seamless communication between interested parties

---

## 2. Core Functionalities

### 2.1 User Management & Authentication
- **User Registration & Login**
  - Email/password authentication
  - Social login (Google, Facebook)
  - Two-factor authentication (2FA)
  - Profile creation and verification

- **User Types**
  - Individual Sellers/Renters
  - Real Estate Agents
  - Professional Agencies
  - Buyers/Renters (with and without accounts)

- **User Profiles**
  - Personal information and contact details
  - Verification badges (phone, email, ID)
  - User ratings and reviews
  - Listing history and saved properties
  - Communication preferences

### 2.2 Property Listings Management
- **Create/Edit Listings**
  - Property type selection (apartment, house, office, land, etc.)
  - Location details (address, GPS coordinates, neighborhood info)
  - Property specifications (size, bedrooms, bathrooms, amenities)
  - Pricing (sale price or rental price)
  - Description and title
  - High-quality image uploads (min 10 photos, max 50)
  - 360° virtual tours
  - Floor plans
  - Highlight/premium listing options

- **Listing States**
  - Draft
  - Active (published)
  - Sold/Rented
  - Archived
  - Expired (automatic after 90 days)
  - Deactivated (user removal)

- **Listing Features**
  - Automatic address geocoding
  - Listing duplication (for agents managing multiple similar properties)
  - Bulk listing operations
  - Expiration and renewal management
  - Featured/highlighted listings with analytics

### 2.3 Advanced Search & Filtering
- **Search Parameters**
  - Location (city, neighborhood, radius search)
  - Property type
  - Price range (min/max)
  - Size range (m²)
  - Number of bedrooms/bathrooms
  - Property condition (new, good, needs reform)
  - Amenities (pool, parking, garden, etc.)
  - Distance to transit/schools/landmarks
  - Property age

- **Search Features**
  - Map-based search interface
  - List/grid/map view toggle
  - Save searches
  - Search alerts and notifications
  - Recently viewed properties
  - Recently added properties

### 2.4 Property Valuation & Analytics
- **Automatic Valuation Model (AVM)**
  - Price estimation based on location, size, amenities
  - Market price trends and comparables
  - Price history for properties
  - Neighborhood statistics

- **Market Insights**
  - Price trends by neighborhood
  - Supply/demand analysis
  - Average days on market
  - Most viewed areas
  - Price per square meter statistics

### 2.5 User Communication System
- **Direct Messaging**
  - In-app messaging between users
  - Message notifications
  - Message history
  - Attachment support (documents, images)

- **Inquiry Management**
  - Property inquiry forms (for anonymous users)
  - Inquiry notifications
  - Response management
  - Inquiry tracking

- **Scheduling**
  - Schedule property viewings
  - Calendar integration
  - View request notifications
  - Viewing history

### 2.6 Favorites & Wishlist
- **Save Properties**
  - Add/remove favorites
  - Create custom collections (wishlist)
  - Organize by criteria
  - Share wishlist with others

- **Notifications**
  - Price drop alerts
  - New property alerts in saved searches
  - Email/SMS notifications
  - Notification preferences customization

### 2.7 User Reviews & Ratings
- **Seller/Agent Reviews**
  - Star ratings (1-5 stars)
  - Written reviews
  - Review verification
  - Response to reviews

- **Property Reviews** (for rentals/past transactions)
  - Neighborhood reviews
  - Property condition accuracy reviews

### 2.8 Real Estate Agent/Agency Tools
- **Agent Dashboard**
  - Portfolio of listings
  - Performance analytics
  - Inquiry and lead management
  - Client management
  - Scheduled viewings calendar

- **Agency Management**
  - Multi-user team access
  - Permission management (admin, agent, viewer)
  - Shared listing portfolios
  - Agency branding

- **Marketing Tools**
  - Featured listings
  - Listing promotion options
  - Email campaigns to saved leads
  - CRM integration ready

### 2.9 Payment & Monetization
- **Listing Packages**
  - Free basic listing
  - Premium listings with extended visibility
  - Featured/highlighted listings
  - Photography/video services

- **Payment Processing**
  - Stripe/PayPal integration
  - Credit card payments
  - Invoice generation
  - Subscription management

### 2.10 Admin & Moderation
- **Content Moderation**
  - Listing approval workflow
  - Spam and fraud detection
  - Manual review queue
  - Content removal and user warnings

- **Platform Analytics**
  - User statistics
  - Listing statistics
  - Search trends
  - Revenue analytics

- **User Management**
  - User ban/suspension
  - Account verification status
  - User activity monitoring

---

## 3. Technical Architecture

### 3.1 Frontend Architecture
**Tech Stack:**
- React.js / Next.js for web application
- React Native / Flutter for mobile (optional)
- TypeScript for type safety
- Redux/Zustand for state management
- Material-UI or Tailwind CSS for styling
- Mapbox or Google Maps API for map features
- Axios for HTTP requests

**Key Components:**
- Property search interface with map
- Listing creation/edit forms with image uploads
- User dashboard and profile management
- Messaging interface
- Admin moderation dashboard

### 3.2 Backend Architecture
**Tech Stack:**
- Node.js with Express.js or Python/Django
- PostgreSQL for relational data
- Redis for caching and session management
- Elasticsearch for advanced search and analytics
- MinIO/AWS S3 for image storage
- Socket.io for real-time features (messaging, notifications)

**Core Services:**
- User authentication & authorization
- Property listing management
- Search and filtering engine
- Messaging system
- Payment processing
- Email notifications
- Image processing and storage
- Analytics and reporting

### 3.3 Infrastructure
- Cloud platform: AWS/Google Cloud/Azure
- Container orchestration: Kubernetes/Docker Compose
- Load balancing and auto-scaling
- CDN for image delivery
- Monitoring and logging (ELK Stack, Sentry)
- CI/CD pipeline (GitHub Actions, GitLab CI)

### 3.4 Security Considerations
- HTTPS/TLS encryption
- OWASP compliance
- SQL injection prevention (parameterized queries)
- XSS protection
- CSRF tokens
- Rate limiting
- Input validation and sanitization
- Data privacy (GDPR compliance)
- Secure password hashing (bcrypt/Argon2)
- API authentication (JWT tokens)

---

## 4. User Flows

### 4.1 Buyer/Renter User Flow
```
1. Visit homepage
   ↓
2. Search for properties (by location, type, price, etc.)
   ↓
3. Browse search results (map/list/grid view)
   ↓
4. View property details
   ↓
5. Save to favorites / Add to wishlist
   ↓
6. Contact seller/agent (message or schedule viewing)
   ↓
7. Receive notifications (price drops, new listings, responses)
   ↓
8. Schedule and attend viewing
   ↓
9. Make purchase/rental agreement
```

### 4.2 Seller/Property Owner Flow
```
1. Sign up and create account
   ↓
2. Verify identity
   ↓
3. Create new listing
   - Fill property details
   - Upload photos/videos
   - Set price
   ↓
4. Publish listing
   ↓
5. Monitor listing performance (views, inquiries)
   ↓
6. Respond to inquiries and messages
   ↓
7. Schedule viewings
   ↓
8. Mark as sold/rented/archived
```

### 4.3 Real Estate Agent Flow
```
1. Sign up as professional agent
   ↓
2. Create agency/join agency
   ↓
3. Get verified badge
   ↓
4. Create multiple listings
   ↓
5. Use agent dashboard
   - View portfolio performance
   - Manage leads and inquiries
   - Schedule client viewings
   ↓
6. Purchase premium services (if needed)
   ↓
7. Monitor analytics and trends
   ↓
8. Export reports
```

### 4.4 Admin Moderation Flow
```
1. Access admin dashboard
   ↓
2. Review new listings in approval queue
   ↓
3. Check flagged content (spam, inappropriate)
   ↓
4. Take action (approve, reject, remove)
   ↓
5. Monitor platform metrics
   ↓
6. Manage users (ban, warn, verify)
```

---

## 5. Database Schema

### 5.1 Core Tables

#### users
```sql
- id (UUID, Primary Key)
- email (String, Unique)
- password_hash (String)
- first_name (String)
- last_name (String)
- phone (String, Nullable)
- profile_photo_url (String, Nullable)
- user_type (Enum: 'individual', 'agent', 'agency')
- bio (Text, Nullable)
- is_verified (Boolean, Default: false)
- verification_type (Enum: 'phone', 'email', 'id', Nullable)
- created_at (Timestamp)
- updated_at (Timestamp)
- last_login (Timestamp, Nullable)
- is_active (Boolean, Default: true)
```

#### properties
```sql
- id (UUID, Primary Key)
- user_id (UUID, Foreign Key → users)
- title (String)
- description (Text)
- property_type (Enum: 'apartment', 'house', 'office', 'land', 'garage', 'other')
- address (String)
- postal_code (String)
- city (String)
- region (String)
- country (String)
- latitude (Decimal)
- longitude (Decimal)
- total_area_m2 (Integer)
- bedrooms (Integer)
- bathrooms (Integer)
- price (Decimal)
- listing_type (Enum: 'for_sale', 'for_rent')
- rental_frequency (Enum: 'monthly', 'yearly', Nullable)
- property_condition (Enum: 'new', 'good', 'needs_reform')
- status (Enum: 'draft', 'active', 'sold', 'archived', 'expired')
- views_count (Integer, Default: 0)
- is_featured (Boolean, Default: false)
- featured_until (Timestamp, Nullable)
- created_at (Timestamp)
- updated_at (Timestamp)
- expired_at (Timestamp, Nullable)
```

#### amenities
```sql
- id (UUID, Primary Key)
- property_id (UUID, Foreign Key → properties)
- amenity_type (String: 'pool', 'parking', 'garden', 'terrace', 'elevator', 'ac', 'heating', etc.)
- created_at (Timestamp)
```

#### property_images
```sql
- id (UUID, Primary Key)
- property_id (UUID, Foreign Key → properties)
- image_url (String)
- image_order (Integer)
- is_main_image (Boolean)
- created_at (Timestamp)
```

#### property_valuations
```sql
- id (UUID, Primary Key)
- property_id (UUID, Foreign Key → properties)
- estimated_value (Decimal)
- valuation_confidence (Integer: 1-100)
- price_per_m2 (Decimal)
- neighborhood_avg_price_m2 (Decimal)
- comparable_properties_count (Integer)
- created_at (Timestamp)
```

#### messages
```sql
- id (UUID, Primary Key)
- sender_id (UUID, Foreign Key → users)
- recipient_id (UUID, Foreign Key → users)
- property_id (UUID, Foreign Key → properties, Nullable)
- subject (String, Nullable)
- body (Text)
- is_read (Boolean, Default: false)
- read_at (Timestamp, Nullable)
- created_at (Timestamp)
- deleted_by_sender (Boolean, Default: false)
- deleted_by_recipient (Boolean, Default: false)
```

#### favorites
```sql
- id (UUID, Primary Key)
- user_id (UUID, Foreign Key → users)
- property_id (UUID, Foreign Key → properties)
- collection_name (String, Default: 'Favorites')
- created_at (Timestamp)
- Unique(user_id, property_id)
```

#### viewings
```sql
- id (UUID, Primary Key)
- property_id (UUID, Foreign Key → properties)
- user_id (UUID, Foreign Key → users) - interested buyer/renter
- agent_id (UUID, Foreign Key → users) - agent showing property
- scheduled_date (Timestamp)
- status (Enum: 'scheduled', 'completed', 'cancelled')
- notes (Text, Nullable)
- created_at (Timestamp)
- updated_at (Timestamp)
```

#### reviews
```sql
- id (UUID, Primary Key)
- reviewer_id (UUID, Foreign Key → users)
- reviewed_user_id (UUID, Foreign Key → users)
- property_id (UUID, Foreign Key → properties, Nullable)
- rating (Integer: 1-5)
- comment (Text)
- is_verified_transaction (Boolean)
- created_at (Timestamp)
- updated_at (Timestamp)
```

#### search_preferences
```sql
- id (UUID, Primary Key)
- user_id (UUID, Foreign Key → users)
- name (String)
- property_type (String, Nullable)
- location (String, Nullable)
- min_price (Decimal, Nullable)
- max_price (Decimal, Nullable)
- min_bedrooms (Integer, Nullable)
- max_bedrooms (Integer, Nullable)
- min_area_m2 (Integer, Nullable)
- alerts_enabled (Boolean, Default: true)
- created_at (Timestamp)
- updated_at (Timestamp)
```

#### agencies
```sql
- id (UUID, Primary Key)
- agency_name (String)
- description (Text, Nullable)
- logo_url (String, Nullable)
- phone (String)
- email (String)
- address (String)
- website (String, Nullable)
- created_at (Timestamp)
- updated_at (Timestamp)
```

#### agency_members
```sql
- id (UUID, Primary Key)
- agency_id (UUID, Foreign Key → agencies)
- user_id (UUID, Foreign Key → users)
- role (Enum: 'admin', 'agent', 'viewer')
- joined_at (Timestamp)
```

#### transactions
```sql
- id (UUID, Primary Key)
- user_id (UUID, Foreign Key → users)
- property_id (UUID, Foreign Key → properties, Nullable)
- amount (Decimal)
- transaction_type (Enum: 'listing_premium', 'featured_listing', 'service')
- status (Enum: 'pending', 'completed', 'failed', 'refunded')
- payment_method (String)
- stripe_charge_id (String, Nullable)
- created_at (Timestamp)
- updated_at (Timestamp)
```

#### notifications
```sql
- id (UUID, Primary Key)
- user_id (UUID, Foreign Key → users)
- type (Enum: 'message', 'viewing', 'price_drop', 'new_listing', 'inquiry', 'favorite_updated')
- title (String)
- body (Text)
- related_property_id (UUID, Foreign Key → properties, Nullable)
- is_read (Boolean, Default: false)
- created_at (Timestamp)
```

---

## 6. API Endpoints

### 6.1 Authentication Endpoints
```
POST   /api/v1/auth/register
POST   /api/v1/auth/login
POST   /api/v1/auth/logout
POST   /api/v1/auth/refresh-token
POST   /api/v1/auth/verify-email
POST   /api/v1/auth/forgot-password
POST   /api/v1/auth/reset-password
POST   /api/v1/auth/2fa/setup
POST   /api/v1/auth/2fa/verify
```

### 6.2 User Profile Endpoints
```
GET    /api/v1/users/profile
PATCH  /api/v1/users/profile
POST   /api/v1/users/profile/verify
GET    /api/v1/users/:id
GET    /api/v1/users/:id/reviews
POST   /api/v1/users/profile-photo
DELETE /api/v1/users/account
```

### 6.3 Property Listing Endpoints
```
POST   /api/v1/properties
GET    /api/v1/properties
GET    /api/v1/properties/:id
PATCH  /api/v1/properties/:id
DELETE /api/v1/properties/:id
POST   /api/v1/properties/:id/publish
POST   /api/v1/properties/:id/archive
POST   /api/v1/properties/:id/images
DELETE /api/v1/properties/:id/images/:imageId
GET    /api/v1/properties/:id/valuation
GET    /api/v1/properties/user/:userId
```

### 6.4 Search & Filter Endpoints
```
GET    /api/v1/search
GET    /api/v1/search/map
POST   /api/v1/search-preferences
GET    /api/v1/search-preferences
DELETE /api/v1/search-preferences/:id
```

### 6.5 Favorites & Wishlist Endpoints
```
POST   /api/v1/favorites
DELETE /api/v1/favorites/:id
GET    /api/v1/favorites
POST   /api/v1/collections
GET    /api/v1/collections
PATCH  /api/v1/collections/:id
DELETE /api/v1/collections/:id
```

### 6.6 Messaging Endpoints
```
POST   /api/v1/messages
GET    /api/v1/messages
GET    /api/v1/messages/:conversationId
PATCH  /api/v1/messages/:id/read
DELETE /api/v1/messages/:id
GET    /api/v1/conversations
```

### 6.7 Viewing/Appointment Endpoints
```
POST   /api/v1/viewings
GET    /api/v1/viewings
PATCH  /api/v1/viewings/:id
DELETE /api/v1/viewings/:id
GET    /api/v1/viewings/calendar
```

### 6.8 Reviews & Ratings Endpoints
```
POST   /api/v1/reviews
GET    /api/v1/reviews/:userId
PATCH  /api/v1/reviews/:id
DELETE /api/v1/reviews/:id
```

### 6.9 Agency Endpoints
```
POST   /api/v1/agencies
GET    /api/v1/agencies/:id
PATCH  /api/v1/agencies/:id
POST   /api/v1/agencies/:id/members
GET    /api/v1/agencies/:id/members
DELETE /api/v1/agencies/:id/members/:userId
GET    /api/v1/agencies/:id/properties
GET    /api/v1/agencies/:id/analytics
```

### 6.10 Payment Endpoints
```
POST   /api/v1/payments/create-intent
POST   /api/v1/payments/confirm
GET    /api/v1/payments/history
GET    /api/v1/invoices/:id
```

### 6.11 Notifications Endpoints
```
GET    /api/v1/notifications
PATCH  /api/v1/notifications/:id/read
PATCH  /api/v1/notifications/read-all
DELETE /api/v1/notifications/:id
GET    /api/v1/notifications/preferences
PATCH  /api/v1/notifications/preferences
```

### 6.12 Admin Endpoints
```
GET    /api/v1/admin/dashboard
GET    /api/v1/admin/listings/pending
POST   /api/v1/admin/listings/:id/approve
POST   /api/v1/admin/listings/:id/reject
GET    /api/v1/admin/users
POST   /api/v1/admin/users/:id/ban
POST   /api/v1/admin/users/:id/verify
GET    /api/v1/admin/reports
GET    /api/v1/admin/analytics
```

---

## 7. Implementation Notes

### 7.1 Phase 1: MVP (Weeks 1-8)
**Core Features:**
- User registration and authentication
- Basic property listing creation and viewing
- Simple search and filtering
- Favorites system
- Direct messaging between users
- Basic user profiles
- Basic property images upload

**Tech Setup:**
- Project initialization (frontend & backend repos)
- Database schema setup
- Authentication system implementation
- API framework setup
- Deployment pipeline

### 7.2 Phase 2: Enhanced Features (Weeks 9-16)
**Features:**
- Advanced search with map interface
- Agent/Agency functionality
- Viewing scheduling system
- Reviews and ratings system
- Payment integration for premium listings
- Email notifications
- Search preferences and alerts
- Property valuation algorithm

### 7.3 Phase 3: Analytics & Optimization (Weeks 17-24)
**Features:**
- Comprehensive analytics dashboards
- Admin moderation tools
- Real estate market insights
- Performance optimization
- Mobile app development (optional)
- Advanced reporting
- CRM features for agents
- 360° virtual tours support

### 7.4 Phase 4: Scale & Polish (Weeks 25+)
**Features:**
- AI-powered recommendations
- Machine learning price prediction
- Advanced fraud detection
- Multi-language support
- International expansion
- Performance tuning
- Enhanced security measures

### 7.5 Development Guidelines

**Code Standards:**
- Consistent naming conventions
- Code comments for complex logic
- Unit test coverage (min 70%)
- Integration tests for APIs
- ESLint/Prettier for code formatting
- Pre-commit hooks for quality checks

**Database:**
- Migration versioning
- Regular backups
- Query optimization
- Indexing on frequently searched columns
- Archive old data regularly

**API Development:**
- RESTful API design
- Consistent error handling
- Rate limiting
- API versioning
- Comprehensive API documentation (Swagger/OpenAPI)
- Input validation and sanitization

**Security:**
- Regular security audits
- Penetration testing
- Dependency vulnerability scanning
- Secrets management (env variables)
- GDPR compliance for user data
- PCI DSS compliance for payments

**Performance Optimization:**
- Image optimization and CDN
- Database query optimization
- Caching strategies (Redis)
- Lazy loading on frontend
- API response pagination
- Request deduplication

**Testing:**
- Unit tests for business logic
- Integration tests for API endpoints
- End-to-end tests for critical user flows
- Performance/load testing
- Security testing

**Monitoring & Logging:**
- Real-time error tracking (Sentry)
- Server logs aggregation
- Performance monitoring
- User analytics tracking
- Alert system for critical errors

### 7.6 Deployment Strategy

**Staging Environment:**
- Pre-production environment mirroring production
- Automated testing before deployment
- Manual QA before production release

**Production Deployment:**
- Blue-green deployment strategy
- Automated backups before deployment
- Rollback procedures
- Infrastructure as Code (Terraform/CloudFormation)
- Auto-scaling configuration

### 7.7 Success Metrics

**User Metrics:**
- Monthly active users (MAU)
- User retention rate
- Conversion rate (searches → inquiries)
- Average session duration
- User engagement score

**Business Metrics:**
- Number of active listings
- Average listing visibility
- Premium listing conversion rate
- Payment processing success rate
- Revenue per user

**Technical Metrics:**
- API response time (target: <200ms)
- System uptime (target: 99.9%)
- Page load time (target: <3s)
- Database query performance
- Error rate (target: <0.1%)

### 7.8 Future Enhancements

- **Mobile Applications:** Native iOS/Android apps
- **AI Features:** Property recommendations, price prediction
- **Virtual Reality:** 3D property tours
- **IoT Integration:** Smart home features listing
- **Blockchain:** Property deed management, smart contracts
- **Social Features:** Property discussion forums, neighborhood communities
- **Video Features:** Agent video tours, live virtual showings
- **Insurance Integration:** Property insurance quotes
- **Financing Tools:** Mortgage calculator, loan pre-approval

---

## 8. Glossary

| Term | Definition |
|------|-----------|
| **AVM** | Automated Valuation Model - algorithm for property price estimation |
| **Featured Listing** | Premium visibility listing at top of search results |
| **Inquiry** | Contact request from interested buyer/renter |
| **Valuation** | Estimated property market value |
| **Viewing** | Scheduled property inspection appointment |
| **Wishlist** | Custom collection of saved properties |
| **Agency** | Professional real estate company |
| **Listing** | Property advertisement posted on platform |
| **Verification** | Process confirming user identity or contact details |

---

## 9. Compliance & Legal

- **Data Protection:** GDPR, CCPA compliance
- **Payment Processing:** PCI DSS compliance
- **Accessibility:** WCAG 2.1 AA standards
- **Terms of Service:** Clear policies on user conduct
- **Privacy Policy:** Transparent data handling practices
- **Content Guidelines:** Restrictions on listings and user conduct
- **Dispute Resolution:** Clear procedures for handling complaints
- **Real Estate Regulations:** Compliance with local real estate licensing requirements

---

**Document Version:** 1.0
**Last Updated:** 2024
**Status:** Initial Specification
