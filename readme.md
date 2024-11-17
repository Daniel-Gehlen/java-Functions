# Technical Report: Java Programs for Calculations in Business and Academia

### Introduction

This project consists of three Java programs designed to address distinct but related calculation needs: computing the area of a circle, determining the adjusted salary of an employee after a percentage increase, and calculating a professor's net salary after deductions. Each program serves a specific use case and is written in Java for simplicity and versatility.

---

## **1. Area Calculation for a Circle**

### **Technical Aspects**
- **Input**: The program accepts the circle's radius as input.
- **Processing**: 
  - The area is calculated using the formula \( \text{Area} = \pi \times \text{radius}^2 \), where \( \pi \) is approximated to 3.14159.
  - It utilizes the `System.console().readLine()` method to read user input and the `Double.parseDouble()` method to convert the input to a double.
- **Output**: Prints the calculated area using `System.out.printf` for formatted output.

### **Use Case**
This program is useful in academic and industrial settings where quick and accurate area calculations are required, such as geometry problems, material usage estimations, or designing circular components.

### **Code Snippet**
```java
double raio, area;
System.out.print("Informe o raio da circunferencia: ");
raio = Double.parseDouble(System.console().readLine());
area = 3.14159 * raio * raio;
System.out.printf("Area da circunferencia = %f\n", area);
```

---

## **2. Adjusted Salary Calculation**

### **Technical Aspects**
- **Input**: The user provides the current salary and the percentage increase.
- **Processing**: 
  - Computes the adjustment value as \( \text{Increase} = \text{Current Salary} \times \text{Percentage} / 100 \).
  - Determines the new salary by adding the increase to the current salary.
  - Utilizes `System.console().readLine()` for input and `Double.parseDouble()` for type conversion.
- **Output**: Displays both the adjustment value and the new salary, formatted to two decimal places using `System.out.printf`.

### **Use Case**
This program is ideal for human resources departments or managers to quickly calculate salary adjustments during performance reviews or cost-of-living adjustments.

### **Code Snippet**
```java
double salario_atual, perc_aumento;
double novo_sal, val_aumento;

System.out.print("Salário atual do funcionário: ");
salario_atual = Double.parseDouble(System.console().readLine());
System.out.print("Percentual de aumento: ");
perc_aumento = Double.parseDouble(System.console().readLine());

val_aumento = salario_atual * perc_aumento / 100;
novo_sal = salario_atual + val_aumento;

System.out.printf("Valor do aumento = R$ %.2f\n", val_aumento);
System.out.printf("Novo salário = R$ %.2f", novo_sal);
```

---

## **3. Net Salary Calculation for Professors**

### **Technical Aspects**
- **Input**: 
  - Hourly rate for teaching, total hours worked, and the percentage of deduction for social security (INSS).
- **Processing**:
  - Gross salary is calculated as \( \text{Gross Salary} = \text{Hourly Rate} \times \text{Hours Worked} \).
  - INSS deduction is computed as \( \text{Deduction} = \text{Gross Salary} \times \text{Percentage} / 100 \).
  - Net salary is determined by subtracting the deduction from the gross salary.
- **Output**: Displays the net salary, formatted to two decimal places.

### **Use Case**
This tool assists professors or educational institutions in estimating net earnings after mandatory deductions, streamlining financial planning.

### **Code Snippet**
```java
double valor_hora, perc_inss;
double sal_bruto, desc_inss, sal_liq;
int horas_trab;

System.out.print("Valor da hora-aula: ");
valor_hora = Double.parseDouble(System.console().readLine());
System.out.print("Numero de horas trabalhadas: ");
horas_trab = Integer.parseInt(System.console().readLine());
System.out.print("Percentual de desconto INSS: ");
perc_inss = Double.parseDouble(System.console().readLine());

sal_bruto = valor_hora * horas_trab;
desc_inss = perc_inss / 100 * sal_bruto;
sal_liq = sal_bruto - desc_inss;

System.out.printf("Salario liquido do professor = R$ %.2f", sal_liq);
```

---

## **General Observations**
- **Portability**: These programs are lightweight and can run on any Java-supported platform.
- **Ease of Use**: With minimal input requirements and a straightforward design, they cater to non-technical users in professional settings.
- **Scalability**: While basic, these programs can be extended for more complex calculations, such as integrating tax brackets or additional deductions.

---

### Conclusion

These Java programs are practical tools tailored for specific financial and academic purposes. Their clear and modular design ensures usability across various domains, providing efficient solutions for everyday computational tasks.