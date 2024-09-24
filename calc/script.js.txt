function converter() {
    real = parseFloat(document.getElementById('real').value) || 0;
    dolar = parseFloat(document.getElementById('dolar').value) || 0;
    euro = parseFloat(document.getElementById('euro').value) || 0;

    if (real !== 0) {
        document.getElementById('dolar').value = (real / 4.5).toFixed(2);
        document.getElementById('euro').value = (real / 5.15).toFixed(2);
    } else if (dolar !== 0) {
        document.getElementById('real').value = (dolar * 4.5).toFixed(2);
        document.getElementById('euro').value = ((dolar * 4.5) / 5.2).toFixed(2);
    } else if (euro !== 0) {
        document.getElementById('real').value = (euro * 5.15).toFixed(2);
        document.getElementById('dolar').value = ((euro * 5.15) / 4.5).toFixed(2);
    }
}

function limpar() {
    document.getElementById('real').value = '';
    document.getElementById('dolar').value = '';
    document.getElementById('euro').value = '';
}

