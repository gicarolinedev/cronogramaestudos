document.addEventListener("DOMContentLoaded", () => {

    // Função para adicionar tarefa
    const botoesAdicionar = document.querySelectorAll('.add-tarefa');
    botoesAdicionar.forEach(botao => {
        botao.addEventListener('click', function () {
            const semana = botao.closest('.semana');
            const inputTarefa = semana.querySelector('.input-tarefa');
            inputTarefa.style.display = 'block';  // Exibe o campo para adicionar tarefa
        });
    });

    // Função para salvar tarefa
    const botoesSalvar = document.querySelectorAll('.salvar-tarefa');
    botoesSalvar.forEach(botao => {
        botao.addEventListener('click', function () {
            const semana = botao.closest('.semana');
            const inputCampo = semana.querySelector('.campo-tarefa');
            const tarefaTexto = inputCampo.value.trim(); // Remove espaços extras

            if (tarefaTexto) {
                const listaTarefas = semana.querySelector('.lista-tarefas');
                const novaTarefa = document.createElement('li');
                novaTarefa.textContent = tarefaTexto;

                // Adiciona botão de Editar
                const botaoEditar = document.createElement('button');
                botaoEditar.textContent = 'Editar';
                botaoEditar.classList.add('editar-tarefa');
                novaTarefa.appendChild(botaoEditar);

                // Adiciona botão de Alterar Status
                const botaoStatus = document.createElement('button');
                botaoStatus.textContent = 'Alterar Status';
                botaoStatus.classList.add('alterar-status');
                novaTarefa.appendChild(botaoStatus);

                // Evento de edição de tarefa
                botaoEditar.addEventListener('click', () => {
                    const novoTexto = prompt("Edite a tarefa:", tarefaTexto);
                    if (novoTexto !== null && novoTexto.trim() !== "") {
                        novaTarefa.firstChild.textContent = novoTexto;
                    }
                });

                // Evento de alterar status
                botaoStatus.addEventListener('click', () => {
                    novaTarefa.classList.toggle('status-em-andamento');
                    novaTarefa.classList.toggle('status-concluido');
                });

                listaTarefas.appendChild(novaTarefa);
                inputCampo.value = ''; // Limpa o campo de entrada
                semana.querySelector('.input-tarefa').style.display = 'none'; // Esconde o campo de tarefa
            }
        });
    });

    // Função para alterar a data
    const botoesAlterarData = document.querySelectorAll('.alterar-data');
    botoesAlterarData.forEach(botao => {
        botao.addEventListener('click', function () {
            const semana = botao.closest('.semana');
            const inputData = semana.querySelector('.data-semana');
            inputData.style.display = 'block';  // Exibe o campo de data
            inputData.focus();

            inputData.addEventListener('blur', () => {
                const novaData = inputData.value.trim();
                if (novaData) {
                    const spanData = semana.querySelector('.data span');
                    spanData.textContent = novaData;  // Atualiza a data na semana
                }
                inputData.style.display = 'none'; // Esconde o campo de data
            });
        });
    });

});
