from scapy.all import sniff, IP, TCP, UDP

print("-" * 50)
print("Starting Advanced Network Sniffer...")
print("Listening for 10 packets (Open Firefox to trigger)")
print("-" * 50)

def process_packet(packet):
    if packet.haslayer(IP):
        src = packet[IP].src
        dst = packet[IP].dst
        
        # Identify the protocol
        proto = "OTHER"
        if packet.haslayer(TCP):
            proto = "TCP (Web/Secure)"
        elif packet.haslayer(UDP):
            proto = "UDP (DNS/Streaming)"
            
        print(f"[+] {proto:18} | {src} -> {dst}")

# Capture 10 packets
sniff(prn=process_packet, count=10)

print("-" * 50)
print("Analysis Complete!")
