impoer socket

def scan(target, ports):
    for port in range(1,ports + 1):
        scan_port(target, port)


def scan_port(ipadress, port):
    try:
        sock = socket.socket()
        sock.connect((ipadress, port))
        print("[+] Port open " + str(port))
        sock.close()
    except:
        pass

targets = input("[*] Enter Targets To Scan(split them by ,: ")
port = int(input("[*] Enter How Many Ports You Want To Scan: "))

if ',' in targets:
    print("[*] Scanning Multiple Targets")
    for ip_addr in targets.split(','):
        scan(ip_addr.strip(' '), port)
else:
    scan(targets, port)

