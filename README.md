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
