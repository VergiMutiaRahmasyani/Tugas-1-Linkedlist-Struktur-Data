# Tugas-1-Linkedlist-Struktur-Data
class Node:
    def __init__(self, menu, harga):
        self.menu = menu
        self.harga = harga
        self.next = None

class Pesanan:
    def __init__(self):
        # Inisialisasi kepala linkedlist
        self.head = None

    def add_order(self, menu, harga):
        new_node = Node(menu, harga) #Membuat Node baru
        if not self.head :
            #Menjadikan node baru sebagai kepala jika pesanan kosong
            self.head = new_node
        else:
            #inisiasi variabel temp untuk menyimpan informasi sementara
            temp = self.head 
            while temp.next:
                temp = temp.next
            #menambahkan node baru dibelakang node terakhir
            temp.next = new_node
            
    def display_orders(self):
        temp = self.head
        while temp :
            print(f"{temp.menu} - {temp.harga} ") # Menampilkan menu dan total harga
            temp = temp.next
            
    def calculate_total(self):
        total = 0
        temp = self.head
        while temp:
            total += temp.harga
            temp = temp.next
        return total
        # Daftar menu beserta harga
daftar_menu = {
        "Miexue Ice Cream": 5000,
        "Boba Shake": 16000,
        "Mi Sundae": 14000,
        "Mi Ganas": 11000,
        "Creamy Mango Boba": 22000
}

# Inisialisasi list untuk menyimpanan Pesanan
menu_list = Pesanan ()

# Fungsi untuk 
def tampilkan_menu():
    print("---Selamat Datang di D4 MIE Mixue---")
    print("------------------------------------")
    print("\nDAFTAR MENU DAN HARGA :")
    print("------------------------------------")
    
    for menu, harga in daftar_menu.items():
        print(f"{menu} - {harga} ")




            
            
