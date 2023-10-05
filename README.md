# Callback Function

Callback adalah sebuah metode pemanggilan suatu function pada javascript, dimana suatu function dipanggil / di-eksekusi pada function lain dan menjadi sebuah paramater

```js
function buyVeggie(uang, buyFish){ // buyFish disini diterima sebagai parameter
    let sayur = 5000
    console.log(`uang maria sebesar ${uang}`);
    uang -= sayur

    console.log(`maria membeli sayur sebanyak ${sayur}`)
    buyFish(uang) // disini dipanggil function buyFish ini disebut callback function
}


function buyFish(uang){
    let ikan = 5000
    uang -= ikan
    console.log(`setelah membeli sayur maria akan membeli ikan Rp. ${ikan}`);
    console.log(`sisa uang maria sebesar ${uang}`);
}


buyVeggie(100_000, buyFish)
//buyFish dijadikan argument dalam memanggil function buyVeggie, jika sebuah function di jadikan argument dia tidak perlu diinvoke
// pada parameter juga tidak perlu diinvoke dan penamaan dari parameter disesuaikan dengan requirement

//How to declare Arrow Function 
const a = () => {

}
```

jika diliat, callback ini mirip dengan **Modular Function**.. bedanya pada **Modular Function**, function helper tidak dijadikan parameter melain kan diinvoke pada main menu, sedangkan pada **Callback Function** dikirim lewat argument tanpa perlu diinvoke lalu diterima ke paramater dan digunakan pada **Function callback** nya
