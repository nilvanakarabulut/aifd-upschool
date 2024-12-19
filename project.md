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


#I used Gemini in my project.I used Streamlit as the basic framework and visualized my Python codes there. I am currently working in a bank and I thought of a chatbot that would proceed like a survey where the user could choose the appropriate card with surveys such as his/her age, whether he/she likes to travel, how often he/she shops, his/her budget, his/her profession and finally come up with a card suggestion. I added a question in my project asking his/her age and how often he/she travels to understand whether it is focused on travel or shopping. It recommends a young card for someone between the ages of 18-25. It does not recommend it for those under the age of 18. In other conditions, it moves on to the second question and can understand which card is the most advantageous for him/her. As the number of cards increases and the data received from the user increases, this chatbot can be more easily detailed.#


