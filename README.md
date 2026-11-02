# hello-
import streamlit as st

st.title("⚽ الآلة الحاسبة الرياضية")
st.write("أهلاً بك! هذه آلة حاسبة بسيطة وسريعة.")

# إدخال الرقم الأول والثاني
num1 = st.number_input("أدخل الرقم الأول:", value=0.0)
num2 = st.number_input("أدخل الرقم الثاني:", value=0.0)

# اختيار العملية الحسابية
operation = st.selectbox(
    "اختر العملية الحسابية:",
    ("جمع (+)", "طرح (-)", "ضرب (×)", "قسمة (÷)")
)

# زر الحساب
if st.button("احسب النتيجة"):
    if operation == "جمع (+)":
        result = num1 + num2
        st.success(print_result := f"النتيجة: {num1} + {num2} = {result}")
    elif operation == "طرح (-)":
        result = num1 - num2
        st.success(f"النتيجة: {num1} - {num2} = {result}")
    elif operation == "ضرب (×)":
        result = num1 * num2
        st.success(f"النتيجة: {num1} × {num2} = {result}")
    elif operation == "قسمة (÷)":
        if num2 != 0:
            result = num1 / num2
            st.success(f"النتيجة: {num1} ÷ {num2} = {result}")
        else:
            st.error("خطأ: لا يمكن القسمة على الرقم صفر (0)!")
