# Vidasalu-CO
<div class="imc-calculator" style="font-family: Arial, sans-serif; max-width: 400px; margin: 20px auto; padding: 20px; border: 1px solid #ddd; border-radius: 8px; box-shadow: 0 2px 4px rgba(0,0,0,0.1);">
    <h2 style="color: #2c3e50; text-align: center;">Calculadora de IMC</h2>
    
    <div style="margin-bottom: 15px;">
        <label for="imc-weight" style="display: block; margin-bottom: 5px; font-weight: bold;">Peso (kg):</label>
        <input type="number" id="imc-weight" style="width: 100%; padding: 8px; border: 1px solid #ddd; border-radius: 4px;" placeholder="Ej. 70">
    </div>
    
    <div style="margin-bottom: 20px;">
        <label for="imc-height" style="display: block; margin-bottom: 5px; font-weight: bold;">Altura (cm):</label>
        <input type="number" id="imc-height" style="width: 100%; padding: 8px; border: 1px solid #ddd; border-radius: 4px;" placeholder="Ej. 175">
    </div>
    
    <button id="imc-calculate" style="width: 100%; padding: 10px; background-color: #3498db; color: white; border: none; border-radius: 4px; cursor: pointer; font-weight: bold;">Calcular IMC</button>
    
    <div id="imc-result" style="margin-top: 20px; padding: 15px; border-radius: 4px; display: none;">
        <h3 style="margin-top: 0;">Tu resultado:</h3>
        <p id="imc-value" style="font-size: 24px; font-weight: bold; margin-bottom: 10px;"></p>
        <p id="imc-category" style="padding: 8px; border-radius: 4px;"></p>
    </div>
    
    <div style="margin-top: 20px; font-size: 14px; color: #7f8c8d;">
        <p><strong>Clasificación del IMC:</strong></p>
        <ul style="padding-left: 20px; margin-top: 5px;">
            <li>Menos de 18.5: Bajo peso</li>
            <li>18.5 - 24.9: Peso normal</li>
            <li>25 - 29.9: Sobrepeso</li>
            <li>30 o más: Obesidad</li>
        </ul>
    </div>
</div>

<script>
document.getElementById('imc-calculate').addEventListener('click', function() {
    const weight = parseFloat(document.getElementById('imc-weight').value);
    const height = parseFloat(document.getElementById('imc-height').value) / 100; // Convertir cm a m
    
    if (isNaN(weight) || isNaN(height) || height <= 0) {
        alert('Por favor ingresa valores válidos para peso y altura');
        return;
    }
    
    const imc = weight / (height * height);
    const resultDiv = document.getElementById('imc-result');
    const valueP = document.getElementById('imc-value');
    const categoryP = document.getElementById('imc-category');
    
    valueP.textContent = imc.toFixed(1);
    
    let category = '';
    let color = '';
    
    if (imc < 18.5) {
        category = 'Bajo peso';
        color = '#f39c12';
    } else if (imc >= 18.5 && imc < 25) {
        category = 'Peso normal';
        color = '#2ecc71';
    } else if (imc >= 25 && imc < 30) {
        category = 'Sobrepeso';
        color = '#e67e22';
    } else {
        category = 'Obesidad';
        color = '#e74c3c';
    }
    
    categoryP.textContent = category;
    categoryP.style.backgroundColor = color;
    categoryP.style.color = 'white';
    
    resultDiv.style.display = 'block';
});
</script>
1. Desayunos para personas con IMC bajo (Bajo peso) <18.5
Objetivo: Aportar energía, proteínas y grasas saludables para aumentar peso de forma equilibrada.

Batido hipercalórico de plátano y mantequilla de maní

1 plátano maduro

2 cucharadas de mantequilla de maní (o almendra)

1 taza de leche entera (o vegetal con proteína)

1 cucharada de avena

1 cucharadita de miel (opcional)

Preparación: Licúa todo y sirve. Añade semillas de chía o linaza para más nutrientes.

Tostadas con aguacate y huevo

2 rebanadas de pan integral

½ aguacate machacado

1 huevo cocido o revuelto

Semillas de sésamo o queso fresco (opcional)

**2. Desayunos para IMC normal (18.5–24.9)
Objetivo: Mantener un equilibrio de nutrientes y energía.

Bowl de yogur con frutas y granola

1 taza de yogur griego natural

½ taza de frutas frescas (fresas, arándanos, kiwi)

2 cucharadas de granola sin azúcar añadido

1 cucharadita de miel o semillas de chía

Omelette de espinacas y queso

2 huevos batidos

½ taza de espinacas frescas

30 g de queso feta o mozzarella

1 rebanada de pan integral tostado

**3. Desayunos para IMC alto (Sobrepeso u obesidad) ≥25
Objetivo: Controlar calorías, aumentar fibra y proteína para saciedad.

Avena con manzana y canela

½ taza de avena en hojuelas

1 taza de leche descremada o agua

½ manzana picada

Canela y stevia al gusto

Preparación: Cocina la avena, añade manzana y endulza.

Tortilla de claras con vegetales

2 claras de huevo + 1 huevo entero

¼ de pimiento y cebolla picados

Espinacas o champiñones

1 rebanada de pan integral ligero
