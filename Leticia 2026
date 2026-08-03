import streamlit as st
import base64
import os

# CONFIGURAÇÃO
st.set_page_config(page_title="Perfil", layout="wide")

# FUNÇÃO BASE64
def get_base64_image(path):
    if os.path.exists(path):
        with open(path, "rb") as img_file:
            return base64.b64encode(img_file.read()).decode()
    return None

# IMAGENS
img_base64 = get_base64_image("genshim.png.jpg")
zap_base64 = get_base64_image("whatsapp.png")

# TOPO
col1, col2, col3 = st.columns([1,2,1])

with col2:

    if img_base64:
        st.markdown(f"""
        <div style="text-align:center; margin-bottom:40px;">
            <a href="https://genshin.hoyoverse.com/pt/home" target="_blank">
                <img src="data:image/png;base64,{img_base64}"
                     width="350"
                     style="
                        border-radius:15px;
                        box-shadow:0px 0px 15px rgba(0,0,0,0.3);
                     ">
            </a>
        </div>
        """, unsafe_allow_html=True)

# LINHA
st.markdown("---")

# LAYOUT PRINCIPAL
col_left, col_right = st.columns([3,1])

with col_left:

    st.markdown("""
    <h1 style="color:#222;">
    Letícia
    </h1>
    """, unsafe_allow_html=True)

    sub1, sub2 = st.columns([1,3])

    # FOTO PERFIL
    with sub1:

        if os.path.exists("let.png"):
            st.image("let.png", width=250)

    # TEXTO
    with sub2:

        st.markdown("""
        <div style="
            font-size:20px;
            line-height:2;
            text-align:justify;
            margin-top:20px;
        ">

        <b>Sobre Letícia:</b><br><br>

        Letícia é estudante do Ensino Médio no IFPB Campus Itabaiana,
        dedicada aos estudos e interessada em biologia. Ela concluirá o
        ensino médio em 2026 e tem o desejo de cursar biomedicina

        </div>
        """, unsafe_allow_html=True)

    st.link_button(
        " Visitar Site do genshim",
        "https://genshin.hoyoverse.com/pt/home"
    )

# WHATSAPP
if zap_base64:
    st.markdown(f"""
    <div style="text-align:center; margin-top:30px;">

        <a href="https://wa.me/5583996736206" target="_blank">

            <img src="data:image/png;base64,{zap_base64}"
                 width="100">

        </a>

    </div>
    """, unsafe_allow_html=True)
