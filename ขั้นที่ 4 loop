# ขั้นที่ 4: จำลองธุรกรรมทีละรายการด้วย loop อย่างน้อย 300 รายการ
random.seed(612104)
members = {
    f"M{i:03d}": Member(f"M{i:03d}", generate_customer_name(), random.randint(0, 9))
    for i in range(1, 61)
}
queue_system = QueueSystem()
orders = []

for i in range(1, 301):
    member = random.choice(list(members.values())) if random.random() < 0.40 else None
    order = build_random_order(i, member)
    order.confirm_payment(random.choice(DrinkOrder.PAYMENT_METHODS))
    if member:
        member.add_points()

    queue_system.send_to_kds(order)
    queue_system.start_preparing(order)
    order.wait_minutes = random.randint(2, 18)
    queue_system.call_queue(order)
    queue_system.complete_order(order)
    orders.append(order)

assert len(orders) == 300
assert len(queue_system.active_orders) == 0
print(f"จำลองครบ {len(orders)} ออเดอร์ และส่งมอบทุกคิวเรียบร้อย")
     
