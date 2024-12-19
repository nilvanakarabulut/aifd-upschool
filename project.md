# aifd-upschool

import streamlit as st
def kredi_kart_onerisi(yas, seyahat_coklugu):
    """
    Kullanicinin yasina ve seyahat cokluguna gore kredi karti onerisi yapar.
    Args:
        yas: Kullanicinin yasi.
        seyahat_coklugu: Kullanicinin yillik seyahat coklugu.
    Returns:
        str: Onerilen kredi karti turu.
    """
    if 18 <= yas <= 25:
        return "Genc Kart"
    elif seyahat_coklugu in ["Ayda 1", "3 ayda 1"]:
        return "Miles Kart"
    else:
        return "Shop Kart"
def main():
    st.title("Kredi Karti Onerim Sistemi")
    yas = st.number_input("Yasiniz:", min_value=18)
    seyahat_coklugu = st.selectbox("Yilda yaklasik kac kez yurt ici/disi seyahat edersiniz?",
                                   options=["Ayda 1", "3 ayda 1", "6 ayda 1", "Senede 1-2"])
    if st.button("Oneri Al"):
        onerilen_kart = kredi_kart_onerisi(yas, seyahat_coklugu)
        st.success(f"Size {onerilen_kart} onerilir.")
if __name__ == "__main__":
    main()
![image](https://github.com/user-attachments/assets/6de3923d-0668-4bba-a163-c0becff0945a)




