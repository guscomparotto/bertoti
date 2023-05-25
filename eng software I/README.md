# bertoti
•Texto1: We see three critical differences between programming and software engineering: time, scale, and the trade-offs at play. On a software engineering project, engineers need to be more concerned with the passage of time and the eventual need for change. In a software engineering organization, we need to be more concerned about scale and efficiency, both for the software we produce as well as for the organization that is producing it. Finally, as software engineers, we are asked to make more complex decisions with higher-stakes outcomes, often based on imprecise estimates of time and growth.

Comentário: Analisamos três diferenças importantíssimas entre programação e engenharia de software, são elas: tempo, escala e as compensações em jogo.
Em um projeto de engenharia de software, os engenheiros, devem se atentar no tempo e uma eventual necessidade de mudança , visando a escala e a eficiência, tanto para o software, quanto para a organização que o está produzindo.
Os engenheiros de software, não apenas programam, mas programam com análise e planejamento, pois são solicitados a tomar decisões mais complexas com resultados de alto risco, muitas vezes com base em estimativas imprecisas de tempo e crescimento.



• Texto 2: Within Google, we sometimes say, “Software engineering is programming integrated over time.” Programming is certainly a significant part of software engineering: after all, programming is how you generate new software in the first place. If you accept this distinction, it also becomes clear that we might need to delineate between programming tasks (development) and software engineering tasks (development, modification, maintenance). The addition of time adds an important new dimension to programming. Cubes aren’t squares, distance isn’t velocity. Software engineering isn’t programming.

Comentário: Dentro do Google, eles dizem que "Engenharia de software é a programação integrada ao longo do tempo" a programação certamente é uma parte muito significativa da engenharia de software, sendo que por meio dela que é criada um novo software, porém a programação seria apenas a tarefa de desenvolvimento do software, na engenharia de software as tarefas abordam o desenvolvimento, modificação, manutenção do software.


<h2>O que são requisitos</h2>
<p>O que são requisitos: requisitos são necessidade do cliente que irão ditar como o engenheiro de software constrói o software. Eles são separados em duas categorias:</p>
<p>• Requisitos funcionais, que são os requisitos que o programa TEM que ter. por exemplo, um app de mensagens tem que ser capaz de enviar mensagens para outras pessoas</p>
<p>• Requisitos não-funcionais se referem a qualidades do software, por exemplo, o app de mensagem tem que enviar as mensagens rapidamente.</p>

<p>Exemplos de requisitos e seus trade-offs
Segurança:
Tempo para implementar, auditoria, revisão constante de ferramenteas e atualizazções / Menos problemas relacionados a vazamento de dados e coisas do gênero/</p>

<p>Portabilidade:
Preocupação com implementação em vários dispositivos diferentes, revisão constante / Alcance de maior n° de usuários/</p>

<h2>Diagrama de classes</h2>

![diagrama](https://github.com/guscomparotto/bertoti/assets/111641203/6b755631-0b4f-4c4a-b1cf-32d949040875)

```java
  
  //classe 1
import java.util.ArrayList;
import java.util.List;


public class Consultório {
   private String endereco;
   private String horario;
   private List<Funcionarios> listaFuncionarios;
   private List<Paciente> listaPaciente;

    public Consultório(String endereco, String horario) {
        this.endereco = endereco;
        this.horario = horario;
        listaFuncionarios = new ArrayList<>();
        listaPaciente = new ArrayList<>();
    }

    public String getEndereco() {
        return endereco;
    }

    public void setEndereco(String endereco) {
        this.endereco = endereco;
    }

    public String getHorario() {
        return horario;
    }

    public void setHorario(String horario) {
        this.horario = horario;
    }
   
    public void adicionarFuncionario(Funcionarios funcionarios) {
        listaFuncionarios.add(funcionarios);
    }
    
    public void adicionarPaciente(Paciente paciente) {
        listaPaciente.add(paciente);
    }
    
    public void imprimirConsultorio() {
        System.out.println("Endereco: " + endereco);
        System.out.println("Horario de funcionamento: " + horario);
        System.out.println("Funcionarios");
        for (Funcionarios funcionario : listaFuncionarios) {
            funcionario.imprimirFuncionarios();
        }
        System.out.println("Pacientes:");
        for (Paciente paciente : listaPaciente) {
            paciente.imprimirPaciente();
        }
        
    }
}
   
   //classe 2
import java.util.ArrayList;
import java.util.List;
import java.util.Scanner;

public class Paciente {

    private String nome;
    private int id;
    private String especie;
    private String doenca;
    private String raca;
    private String porte;
    private int idade;

    public Paciente(String nome, int id, String especie, String doenca, String raca, String porte, int idade) {
        this.nome = nome;
        this.id = id;
        this.especie = especie;
        this.doenca = doenca;
        this.raca = raca;
        this.porte = porte;
        this.idade = idade;
    }

    
    public String getNome() {
        return nome;
    }
    
    public void setNome(String nome) {
        this.nome = nome;
    }
    
    public int getId() {
        return id;
    }

    public void setId(int id) {
        this.id = id;
    }

    public String getEspecie() {
        return especie;
    }

    public void setEspecie(String especie) {
        this.especie = especie;
    }

    public String getDoenca() {
        return doenca;
    }

    public void setDoenca(String doenca) {
        this.doenca = doenca;
    }

    public String getRaca() {
        return raca;
    }

    public void setRaca(String raca) {
        this.raca = raca;
    }

    public String getPorte() {
        return porte;
    }

    public void setPorte(String porte) {
        this.porte = porte;
    }

    public int getIdade() {
        return idade;
    }

    public void setIdade(int idade) {
        this.idade = idade;
    }

    

    public void imprimirPaciente() {
        System.out.println("Nome:" + nome);
        System.out.println("Id: " + id);
        System.out.println("Especie:" + especie);
        System.out.println("Doenca:" + doenca);
        System.out.println("Raa:" + raca);
        System.out.println("Porte:" + porte);
        System.out.println("Idade:" + idade);
        
    }

    }
    


  //classe 3
public class Funcionarios {
    private String nome;
    private String turno;
    private String salario;

    public Funcionarios(String nome, String turno, String salario) {
        this.nome = nome;
        this.turno = turno;
        this.salario = salario;
    }

    public String getNome() {
        return nome;
    }

    public void setNome(String nome) {
        this.nome = nome;
    }

    public String getTurno() {
        return turno;
    }

    public void setTurno(String turno) {
        this.turno = turno;
    }

    public String getSalario() {
        return salario;
    }

    public void setSalario(String salario) {
        this.salario = salario;
    }
    
    public void imprimirFuncionarios() {
        System.out.println("Nome:" + nome);
        System.out.println("Turno:" + turno);
        System.out.println("Salario:" + salario);
    }
    
}



  

```
