# 💐 Engenharia de Software

Este documento apresenta reflexões sobre a importância da Engenharia de Software, seus princípios e os desafios.  
O conteúdo está dividido em nove partes: uma introdução sobre o tema, uma análise sobre o papel da engenharia de software além da programação, exemplos de **trade-offs** comuns na área, diagramas de classes e códigos em Java.

---

## 🧩 1. Primeiro Trecho

O texto aborda a importância da engenharia de software e a distingue das demais engenharias.  
A proposta é atribuir à engenharia de software o mesmo nível de rigor e relevância presente em outras áreas da engenharia, adotando métodos bem definidos que garantam **qualidade**, **confiabilidade** e **segurança**.  

Isso se torna essencial, pois o software está cada vez mais presente no cotidiano das pessoas e desempenha um papel fundamental no funcionamento de atividades diárias.

---

## 💻 2. Segundo trecho

Tanto o segundo trecho quanto o primeiro mostram que a engenharia de software não se limita apenas à programação ou à escrita de código.  
Ela envolve todo o processo necessário para manter o código utilizável e sustentável ao longo do tempo.  

Para isso, é essencial adotar **princípios sólidos**, lidar com mudanças e garantir **adaptabilidade**.  
Além disso, boas práticas devem ser aplicadas para que o desenvolvimento seja **eficiente e sustentável**, mesmo diante de decisões complexas e **trade-offs**.

---

## ⚖️ 3. Exemplos de Trade-offs

| **Aspecto** | **Descrição** |
|--------------|----------------|
| 🕒 **Velocidade vs. Qualidade** | Entregar rápido pode reduzir a qualidade do código. |
| ⚙️ **Escalabilidade vs. Complexidade** | Projetar um sistema para milhões de usuários desde o início pode deixá-lo desnecessariamente complexo se o uso inicial for pequeno. |
| 💰 **Custo vs. Escalabilidade** | Investir em alta escalabilidade desde o início pode sair caro se ainda não houver demanda. |

---

## 🌸 4. Diagrama da Floricultura

![Diagrama](https://github.com/mavygarcia/bertoti/blob/main/Floricultura.jpg)

---

## 5. Código em Java
**Class Flor**
```Java
import java.util.ArrayList;
import java.util.List;

public class Flor {
    private String nome;
    private double preco;
    private String tipo;

    public Flor(String nome, double preco, String tipo) {
        this.nome = nome;
        this.preco = preco;
        this.tipo = tipo;
    }

    public String getNome() {
        return nome;
    }

    public double getPreco() {
        return preco;
    }

    public String getTipo() {
        return tipo;
    }

    public void setPreco(double preco) {
        this.preco = preco;
    }
}
```
**Class Cliente**
```Java
public class Cliente {
    private String nome;
    private String telefone;
    private String email;

    public Cliente(String nome, String telefone, String email) {
        this.nome = nome;
        this.telefone = telefone;
        this.email = email;
    }

    public String getNome() {
        return nome;
    }

    public String getTelefone() {
        return telefone;
    }

    public String getEmail() {
        return email;
    }
}
```

**Class Pedido**
```Java
import java.util.ArrayList;
import java.util.List;

public class Pedido {
    private int id;
    private Cliente cliente;
    private List<Flor> flores = new ArrayList<>();

    public Pedido(int id, Cliente cliente) {
        this.id = id;
        this.cliente = cliente;
    }

    public void adicionarFlor(Flor flor) {
        flores.add(flor);
    }

    public double calcularTotal() {
        double total = 0;
        for (Flor flor : flores) {
            total += flor.getPreco();
        }
        return total;
    }

    public Cliente getCliente() {
        return cliente;
    }

    public List<Flor> getFlores() {
        return flores;
    }
}
```
---

## 🌼 6. Testes JUnit
```Java
import org.junit.jupiter.api.Test;
import static org.junit.jupiter.api.Assertions.*;

public class PedidoTest {

    @Test
    public void testAdicionarFlorECalcularTotal() {
        Cliente cliente = new Cliente("Marya", "99249-8798", "marya@email.com");
        Pedido pedido = new Pedido(1, cliente);

        Flor tulipa = new Flor("Tulipa", 10.0, "Romântica");
        Flor maragarida = new Flor("Margarida", 8.0, "Solar");

        pedido.adicionarFlor(tulipa);
        pedido.adicionarFlor(margarida);

        assertEquals(2, pedido.getFlores().size());
        assertEquals(18.0, pedido.calcularTotal(), 0.001);
    }

    @Test
    public void testClienteDoPedido() {
        Cliente cliente = new Cliente("Eloa", "98888-7777", "eloa@email.com");
        Pedido pedido = new Pedido(2, cliente);

        assertEquals("Eloa", pedido.getCliente().getNome());
    }
}
```



