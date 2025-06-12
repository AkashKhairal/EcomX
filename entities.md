🧾 product-service
java
Copy
Edit
Product {
    Long id;
    String name;
    String description;
    BigDecimal price;
    String sku;
    Integer quantityAvailable;
    String category;
    String imageUrl;
}
👤 user-service
java
Copy
Edit
User {
    Long id;
    String username;
    String email;
    String passwordHash;
    String fullName;
    String role; // USER, ADMIN
    String phoneNumber;
    LocalDateTime createdAt;
}
📦 order-service
java
Copy
Edit
Order {
    Long id;
    Long userId;
    List<OrderItem> items;
    BigDecimal totalAmount;
    String paymentStatus; // PENDING, SUCCESS, FAILED
    String orderStatus; // PLACED, SHIPPED, DELIVERED
    LocalDateTime orderDate;
}

OrderItem {
    Long productId;
    Integer quantity;
    BigDecimal priceAtPurchase;
}
💳 payment-service
java
Copy
Edit
Payment {
    Long id;
    Long orderId;
    Long userId;
    BigDecimal amount;
    String paymentMethod; // CARD, UPI, NETBANKING
    String paymentStatus; // INITIATED, SUCCESS, FAILED
    LocalDateTime paymentDate;
}
🔐 auth-service (if not using Keycloak)
java
Copy
Edit
AuthRequest {
    String email;
    String password;
}

AuthResponse {
    String jwtToken;
    String refreshToken;
    String role;
}
