# SQL_Optimatization_Project

# Database overview

Database BI postgresql digital skola :



# Latar Belakang dalam Konteks Bisnis: 
Manajemen PT X ingin brief eksekutif tahun berjalan (YTD) untuk menutup kuartal dengan 
strategi yang tepat. Mereka butuh melihat momentum penjualan bulanan, lalu mengecek 
kualitas pengiriman (SLA) agar keluhan tidak meningkat. Setelah itu, mereka ingin fokus pada 
produk yang benar-benar menyumbang pendapatan, menilai performa per sales, dan terakhir 
memahami porsi pelanggan baru vs loyal agar keputusan marketing & retensi lebih tajam. 

Ada 5 Poin yang ingin dilihat oleh management: 

1. Monthly Performance
   
        ● Tujuan bisnis: Amati momentum penjualan bulanan.
      
        ● Pertanyaan: Tampilkan jumlah order, total revenue, dan avg order value per bulan 
        (di tahun 2025). 
        
        ● Tabel: orders, order_details 
        
        ● revenue = unit_price * quantity * (1 - discount).


3. Shipper SLA (YTD)
   
        ● Tujuan bisnis: Evaluasi kurir (SLA).
   
        ● Pertanyaan: Untuk order yang sudah dikirim (YTD), tampilkan per kurir: shipped_orders, late_orders (shipped_date > required_date), dan 
        late_rate_%.
   
        ● Tabel: orders, shippers
   
3. Top 10 Products by Revenue (YTD)
   
        ● Tujuan bisnis: Fokus ke produk penyumbang pendapatan. 
        
        ● Pertanyaan: Tampilkan 10 produk ber-revenue tertinggi (YTD) beserta nama kategori dan price_range (<10, 10–20, 20–50, >50). 
        
        ● Tabel: orders, order_details, products, categories 

4. Sales Rep Scorecard (YTD)
   
        ● Tujuan bisnis: Ringkas performa per sales rep. 
        
        ● Pertanyaan: Per karyawan tampilkan jumlah order, avg order value, dan % order besar (order_total > 1000). 
        
        ● Tabel: orders, order_details, employees 

5. New vs Loyal Customers (YTD)
   
        ● Tujuan bisnis: Pahami porsi akuisisi vs retensi. 
        
        ● Pertanyaan: Segmentasi order YTD ke NEW (first order customer di tahun ini) vs LOYAL (first order sebelum tahun ini). Tampilkan orders dan revenue. 
        
        ● Tabel: orders, order_details 
        
        ● Output: segment, orders, revenue
