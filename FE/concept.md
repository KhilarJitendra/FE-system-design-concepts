---

# Frontend System Design – Senior Engineer Cheat Sheet

---

## 1. Networking & Browser Fundamentals

### How the Web Works

* DNS lookup
* TCP/TLS handshake
* HTTP request/response lifecycle
* Browser caching & connection reuse

### Rendering of a Web Page (Check this - https://www.youtube.com/watch?v=PK4bzxWLOfo )

* HTML → DOM
* CSS → CSSOM
* DOM + CSSOM → Render Tree
* Layout → Paint → Composite
* Reflow vs Repaint (when & why they happen)

### Web Workers (chgeck this - https://www.youtube.com/watch?v=k2RmGMwBPbs)

* Offload heavy computation
* No DOM access
* Improves main-thread responsiveness

---

## 2. Communication Techniques (check this - https://www.youtube.com/watch?v=M2RpzmyKfvQ)

### Real-time Data

* Short polling
* Long polling
* WebSockets
* Server-Sent Events (SSE)

### When to Use What

* Chat / live comments → WebSocket
* Notifications / feeds → SSE
* Simple updates → Polling

---

## 3. API & Data Layer (Check this - https://www.youtube.com/watch?v=M2RpzmyKfvQ)

### API Styles

* REST API
* GraphQL

  * Query vs Mutation
  * Batching
  * Over-fetching vs under-fetching
* gRPC (less common in FE, but good to mention)
   - trpc
     - no need to write heavy API end point
     - Just wrtite function n BE and call from FE same function (but behind the scene it will done via HTTP) somehow simillar to SDK

### Headers & Contracts

* Authorization headers
* Caching headers
* Versioning
* Error handling contracts

---

## 5. Performance

### What to Measure

* FCP, LCP, CLS, TTI
* Bundle size
* API latency
* Interaction delay

### Optimizations

* Build optimization (code splitting, tree shaking)
* Network optimization (HTTP/2, compression)
* Asset optimization (images, fonts)
* JavaScript optimization
* React / Framework optimization

### Rendering Patterns

* CSR
* SSR
* SSG
* RSC (React Server Components)

### Tools

* Lighthouse
* Chrome DevTools
* Web Vitals
* Bundle analyzers

---

## 6. Caching Strategies

### Client-side

* LocalStorage
* SessionStorage
* Cookies

### HTTP Caching

* Cache-Control
* ETag
* Expires

### Application-level

* Service Worker caching
* App shell caching
* Prefetching / preloading

---

## 7. Offline Support (PWA)

* Service Workers
* IndexedDB
* Cache API
* Background sync
* Offline-first strategies (Google Docs example)

---

## 8. Security (Frontend Focused)

### Common Attacks

* XSS
* CSRF
* SSRF
* Injection attacks

### Protection Techniques

* Input/output sanitization
* CORS
* CSP (Content Security Policy)
* Security headers
* Authentication vs Authorization

### Dependency Security

* npm audit
* Dependency updates
* License compliance

---

## 9. Accessibility (a11y)

* Keyboard navigation
* Screen reader support
* ARIA roles
* Color contrast
* Focus management

---

## 10. Logging & Monitoring

* Telemetry
* Error logging
* User behavior tracking
* Performance monitoring

### Tools (Examples)

* Sentry
* Datadog
* Custom logging pipelines

---

## 11. Testing Strategy

### Types of Testing

* Unit testing
* Component testing
* Integration testing
* End-to-End testing (Playwright / Cypress)
* Load testing
* A/B testing

### TDD

* Write tests first
* Improves design clarity

---

## 12. Example Systems You Should Be Able to Design

* Facebook / Instagram Feed
* Google Docs (real-time collaboration)
* Live comments system
* Video streaming UI
* Photo sharing app


## Resources 

- QSTNS - https://www.youtube.com/watch?v=5vyKhm2NTfw&list=PLI9W87-Dqn7j_x6QtR6sUjycJR7nQLBqT&index=2&t=258s 
- Starting - https://www.youtube.com/watch?v=44mOnnt5pic&list=PL4CFloQ4GGWICE0Tz6iXKfN3XWkXRlboU&index=4 
- Performance - https://www.youtube.com/watch?v=zAEy0jchvH8&t=3743s
- Communication - https://www.youtube.com/watch?v=M2RpzmyKfvQ&t=458s
- RADIO FRAMEWORK - https://www.greatfrontend.com/front-end-system-design-playbook/framework

--
ANSWERS
--

1. How the Web Works

<img width="389" height="717" alt="Screenshot 2026-01-04 at 2 35 47 PM" src="https://github.com/user-attachments/assets/37188d4f-2b92-4e67-93cd-59a5207a1ebd" />

- TLS encryption and TCP transmission happen at both endpoints. The client encrypts HTTP data before sending it over TCP, and the server decrypts it after TCP reassembly. The server then encrypts the response and sends it     back the same way

- Before making a request, the browser checks cache. If there’s a miss, it tries to reuse an existing TCP/TLS connection. Only if that’s not possible does it perform DNS lookup and new handshakes before sending the HTTP request.

- HTTP  → defines WHAT data looks like
- TLS   → encrypts the data (only if we have https)
- TCP   → delivers the data reliably
- IP    → routes the packets














