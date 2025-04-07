<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sistema de Carregamento de Caminhões</title>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css">
    <style>
        .time-normal { color: green; }
        .time-warning { color: orange; font-weight: bold; }
        .time-critical { color: red; font-weight: bold; }
        .card-carregamento { transition: all 0.3s; }
        .card-carregamento:hover { transform: translateY(-5px); box-shadow: 0 10px 20px rgba(0,0,0,0.1); }
        .dashboard-card { height: 100%; }
        .codigo-funcionario {
            font-family: monospace;
            font-size: 1.2em;
            letter-spacing: 1px;
            color: #0d6efd;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1 class="text-center mb-4">Sistema de Carregamento de Caminhões</h1>
        
        <ul class="nav nav-tabs" id="myTab" role="tablist">
            <li class="nav-item" role="presentation">
                <button class="nav-link active" id="home-tab" data-bs-toggle="tab" data-bs-target="#home" type="button" role="tab">Operação</button>
            </li>
            <li class="nav-item" role="presentation">
                <button class="nav-link" id="cadastro-tab" data-bs-toggle="tab" data-bs-target="#cadastro" type="button" role="tab">Cadastrar Funcionário</button>
            </li>
            <li class="nav-item" role="presentation">
                <button class="nav-link" id="busca-tab" data-bs-toggle="tab" data-bs-target="#busca" type="button" role="tab">Buscar Funcionário</button>
            </li>
            <li class="nav-item" role="presentation">
                <button class="nav-link" id="dashboard-tab" data-bs-toggle="tab" data-bs-target="#dashboard" type="button" role="tab">Dashboard</button>
            </li>
            <li class="nav-item" role="presentation">
                <button class="nav-link" id="historico-tab" data-bs-toggle="tab" data-bs-target="#historico" type="button" role="tab">Histórico</button>
            </li>
        </ul>
        
        <div class="tab-content" id="myTabContent">
            <!-- ABA PRINCIPAL (OPERAÇÃO) -->
            <div class="tab-pane fade show active" id="home" role="tabpanel">
                <div class="row mt-3">
                    <div class="col-md-6">
                        <div class="card">
                            <div class="card-body">
                                <h5 class="card-title">Operações de Carregamento</h5>
                                <button id="btnIniciarCarregamento" class="btn btn-primary btn-lg w-100 mb-3">Iniciar Carregamento</button>
                                <button id="btnFinalizarCarregamento" class="btn btn-success btn-lg w-100">Finalizar Carregamento</button>
                            </div>
                        </div>
                    </div>
                    <div class="col-md-6">
                        <div class="card">
                            <div class="card-body">
                                <h5 class="card-title">Informações</h5>
                                <p>Digite o código do funcionário para iniciar ou finalizar o carregamento.</p>
                                <p>Os códigos começam com <strong>GZL-EO</strong> seguido de identificação única.</p>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="row mt-3" id="formContainer" style="display: none;">
                    <div class="col-md-6">
                        <div class="card">
                            <div class="card-body">
                                <h5 class="card-title" id="formTitle">Informações do Carregamento</h5>
                                <div class="mb-3">
                                    <label for="funcionarioId" class="form-label">Código do Funcionário</label>
                                    <input type="text" class="form-control" id="funcionarioId" placeholder="Ex: GZL-EO-1234">
                                </div>
                                <div class="mb-3">
                                    <label for="placaCaminhao" class="form-label">Placa do Caminhão</label>
                                    <input type="text" class="form-control" id="placaCaminhao" placeholder="Ex: ABC1234">
                                </div>
                                <button id="btnConfirmar" class="btn btn-primary">Confirmar</button>
                                <button id="btnCancelar" class="btn btn-secondary">Cancelar</button>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="row mt-3">
                    <div class="col-12">
                        <div class="card">
                            <div class="card-body">
                                <h5 class="card-title">Carregamentos em Andamento</h5>
                                <div id="carregamentosAndamento"></div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- ABA DE CADASTRO -->
            <div class="tab-pane fade" id="cadastro" role="tabpanel">
                <div class="row">
                    <div class="col-md-6">
                        <div class="mb-3">
                            <label for="novoNome" class="form-label">Nome Completo</label>
                            <input type="text" class="form-control" id="novoNome" placeholder="Ex: João da Silva">
                        </div>
                        <div class="mb-3">
                            <label for="novoCargo" class="form-label">Cargo</label>
                            <input type="text" class="form-control" id="novoCargo" placeholder="Ex: Carregador">
                        </div>
                        <button id="btnCadastrar" class="btn btn-primary">Cadastrar Funcionário</button>
                    </div>
                    <div class="col-md-6">
                        <div class="card">
                            <div class="card-body">
                                <h5 class="card-title">Código do Funcionário</h5>
                                <div id="codigoGerado" class="codigo-funcionario mb-3" style="display: none;"></div>
                                <div id="infoCadastro"></div>
                                <button id="btnDownloadPDF" class="btn btn-success mt-2" style="display: none;">Download PDF</button>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- ABA DE BUSCA -->
            <div class="tab-pane fade" id="busca" role="tabpanel">
                <div class="row">
                    <div class="col-md-6">
                        <div class="mb-3">
                            <label for="buscarFuncionario" class="form-label">Código do Funcionário</label>
                            <input type="text" class="form-control" id="buscarFuncionario" placeholder="Ex: GZL-EO-1234">
                        </div>
                        <button id="btnBuscar" class="btn btn-info">Buscar</button>
                        <div id="infoFuncionario" class="mt-3"></div>
                    </div>
                </div>
            </div>
            
            <!-- ABA DASHBOARD -->
            <div class="tab-pane fade" id="dashboard" role="tabpanel">
                <div class="row">
                    <div class="col-12">
                        <h3>Dashboard em Tempo Real</h3>
                        <div class="alert alert-info">
                            <strong>Total de Carregamentos Hoje:</strong> <span id="totalCarregamentosHoje">0</span>
                        </div>
                    </div>
                </div>
                
                <div class="row mt-3">
                    <div class="col-md-6">
                        <div class="card dashboard-card">
                            <div class="card-body">
                                <h5 class="card-title">Carregamentos em Andamento</h5>
                                <div id="dashboardCarregamentos"></div>
                            </div>
                        </div>
                    </div>
                    <div class="col-md-6">
                        <div class="card dashboard-card">
                            <div class="card-body">
                                <h5 class="card-title">Funcionários em Ação</h5>
                                <div id="dashboardFuncionarios"></div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- ABA HISTÓRICO -->
            <div class="tab-pane fade" id="historico" role="tabpanel">
                <div class="row">
                    <div class="col-md-4">
                        <div class="mb-3">
                            <label for="filtroMes" class="form-label">Mês</label>
                            <select class="form-select" id="filtroMes">
                                <option value="01">Janeiro</option>
                                <option value="02">Fevereiro</option>
                                <option value="03">Março</option>
                                <option value="04">Abril</option>
                                <option value="05">Maio</option>
                                <option value="06">Junho</option>
                                <option value="07">Julho</option>
                                <option value="08">Agosto</option>
                                <option value="09">Setembro</option>
                                <option value="10">Outubro</option>
                                <option value="11">Novembro</option>
                                <option value="12">Dezembro</option>
                            </select>
                        </div>
                    </div>
                    <div class="col-md-4">
                        <div class="mb-3">
                            <label for="filtroAno" class="form-label">Ano</label>
                            <select class="form-select" id="filtroAno">
                                <option value="2023">2023</option>
                                <option value="2024">2024</option>
                                <option value="2025">2025</option>
                            </select>
                        </div>
                    </div>
                    <div class="col-md-4">
                        <div class="mb-3">
                            <label for="filtroFuncionario" class="form-label">Funcionário (opcional)</label>
                            <input type="text" class="form-control" id="filtroFuncionario" placeholder="Código do Funcionário">
                        </div>
                    </div>
                </div>
                
                <div class="row">
                    <div class="col-12">
                        <button id="btnFiltrar" class="btn btn-primary">Filtrar</button>
                    </div>
                </div>
                
                <div class="row mt-3">
                    <div class="col-12">
                        <div class="card">
                            <div class="card-body">
                                <h5 class="card-title">Estatísticas Gerais</h5>
                                <div class="row">
                                    <div class="col-md-4">
                                        <div class="card bg-light mb-3">
                                            <div class="card-body">
                                                <h6 class="card-title">Total de Caminhões</h6>
                                                <p class="display-4 text-center" id="totalCaminhoes">0</p>
                                            </div>
                                        </div>
                                    </div>
                                    <div class="col-md-4">
                                        <div class="card bg-light mb-3">
                                            <div class="card-body">
                                                <h6 class="card-title">Média de Tempo</h6>
                                                <p class="display-4 text-center" id="mediaTempo">0 min</p>
                                            </div>
                                        </div>
                                    </div>
                                    <div class="col-md-4">
                                        <div class="card bg-light mb-3">
                                            <div class="card-body">
                                                <h6 class="card-title">Valor Total</h6>
                                                <p class="display-4 text-center" id="valorTotal">R$ 0,00</p>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="row mt-3">
                    <div class="col-12">
                        <div class="card">
                            <div class="card-body">
                                <h5 class="card-title">Top Funcionários</h5>
                                <div class="table-responsive">
                                    <table class="table table-striped">
                                        <thead>
                                            <tr>
                                                <th>Posição</th>
                                                <th>Funcionário</th>
                                                <th>Carregamentos</th>
                                                <th>Tempo Médio</th>
                                                <th>Valor Ganho</th>
                                            </tr>
                                        </thead>
                                        <tbody id="topFuncionarios">
                                        </tbody>
                                    </table>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="row mt-3">
                    <div class="col-12">
                        <div class="card">
                            <div class="card-body">
                                <h5 class="card-title">Histórico Completo</h5>
                                <div class="table-responsive">
                                    <table class="table table-striped">
                                        <thead>
                                            <tr>
                                                <th>Data</th>
                                                <th>Placa</th>
                                                <th>Funcionário</th>
                                                <th>Início</th>
                                                <th>Fim</th>
                                                <th>Tempo</th>
                                            </tr>
                                        </thead>
                                        <tbody id="tabelaHistorico">
                                        </tbody>
                                    </table>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Modal para detalhes do funcionário -->
    <div class="modal fade" id="modalFuncionario" tabindex="-1" aria-hidden="true">
        <div class="modal-dialog modal-lg">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title" id="modalFuncionarioTitle">Detalhes do Funcionário</h5>
                    <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body" id="modalFuncionarioBody">
                    <!-- Conteúdo será preenchido via JS -->
                </div>
                <div class="modal-footer">
                    <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Fechar</button>
                </div>
            </div>
        </div>
    </div>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/jspdf.umd.min.js"></script>
    <script src="https://www.gstatic.com/firebasejs/9.6.0/firebase-app-compat.js"></script>
    <script src="https://www.gstatic.com/firebasejs/9.6.0/firebase-database-compat.js"></script>
    <script>
        // Inicializa o Firebase
        const firebaseConfig = {
            apiKey: "AIzaSyBAH_sO68BD_vt9J40Hf8rdgLTNQEuEEBc",
            authDomain: "produtividade-bc.firebaseapp.com",
            projectId: "produtividade-bc",
            storageBucket: "produtividade-bc.appspot.com",
            messagingSenderId: "665932698083",
            appId: "1:665932698083:web:1c807c6b1571e3024bd0d6",
            measurementId: "G-608P3H613B"
        };

        // Initialize Firebase
        const app = firebase.initializeApp(firebaseConfig);
        const database = firebase.database();
        
        // Referências do banco de dados
        const funcionariosRef = database.ref('funcionarios');
        const carregamentosRef = database.ref('carregamentos');
        const estatisticasRef = database.ref('estatisticas');
        
        // Variáveis globais
        let operacaoAtual = null; // 'iniciar' ou 'finalizar'
        let carregamentosEmAndamento = {};
        let intervalos = {};
        
        // Gera um código único para o funcionário
        function gerarCodigoFuncionario() {
            const prefixo = "GZL-EO-";
            const randomPart = Math.floor(1000 + Math.random() * 9000); // Número entre 1000 e 9999
            return prefixo + randomPart;
        }
        
        // Gera PDF com o código do funcionário
        function gerarPDFCodigo(codigo, nome, cargo) {
            const { jsPDF } = window.jspdf;
            const doc = new jsPDF();
            
            // Adiciona logo ou título
            doc.setFontSize(20);
            doc.text('Código do Funcionário', 105, 20, { align: 'center' });
            
            // Adiciona informações
            doc.setFontSize(14);
            doc.text('Nome:', 20, 40);
            doc.text(nome, 40, 40);
            
            doc.text('Cargo:', 20, 50);
            doc.text(cargo, 40, 50);
            
            doc.text('Código:', 20, 70);
            doc.setFontSize(24);
            doc.text(codigo, 50, 70);
            
            // Adiciona data de emissão
            doc.setFontSize(10);
            doc.text(`Emitido em: ${new Date().toLocaleDateString()}`, 20, 100);
            
            // Salva o PDF
            doc.save(`codigo-funcionario-${codigo}.pdf`);
        }
        
        // Busca um funcionário pelo ID
        function buscarFuncionario(id, mostrarModal = false) {
            funcionariosRef.child(id).once('value', (snapshot) => {
                const funcionario = snapshot.val();
                
                if (!funcionario) {
                    alert('Funcionário não encontrado!');
                    return;
                }
                
                if (mostrarModal) {
                    mostrarDetalhesFuncionario(id, funcionario);
                }
                
                return funcionario;
            });
        }
        
        // Mostra os detalhes do funcionário em um modal
        function mostrarDetalhesFuncionario(id, funcionario) {
            // Busca os carregamentos do funcionário
            carregamentosRef.orderByChild('funcionarioId').equalTo(id).once('value', (snapshot) => {
                const carregamentos = snapshot.val() || {};
                const carregamentosArray = Object.values(carregamentos);
                
                carregamentosArray.sort((a, b) => (b.inicio || 0) - (a.inicio || 0));
                
                let html = `
                    <div class="row">
                        <div class="col-md-4">
                            <h4><span class="codigo-funcionario">${id}</span></h4>
                            <p><strong>Nome:</strong> ${funcionario.nome || 'Não informado'}</p>
                            <p><strong>Cargo:</strong> ${funcionario.cargo || 'Não informado'}</p>
                            <p><strong>Total de Carregamentos:</strong> ${carregamentosArray.length}</p>
                        </div>
                        <div class="col-md-8">
                            <h5>Últimos Carregamentos</h5>
                            <div class="table-responsive">
                                <table class="table table-sm">
                                    <thead>
                                        <tr>
                                            <th>Data</th>
                                            <th>Placa</th>
                                            <th>Tempo</th>
                                            <th>Status</th>
                                        </tr>
                                    </thead>
                                    <tbody>
                `;
                
                const carregamentosExibir = carregamentosArray.slice(0, 5);
                
                carregamentosExibir.forEach(carregamento => {
                    const inicio = carregamento.inicio ? new Date(carregamento.inicio).toLocaleString() : 'N/A';
                    const fim = carregamento.fim ? new Date(carregamento.fim).toLocaleString() : 'N/A';
                    const tempo = carregamento.fim ? `${((carregamento.fim - carregamento.inicio) / 60000).toFixed(2)} min` : 'Em andamento';
                    const status = carregamento.finalizado ? 'Finalizado' : 'Em andamento';
                    
                    html += `
                        <tr>
                            <td>${inicio.split(',')[0]}</td>
                            <td>${carregamento.placa || 'N/A'}</td>
                            <td>${tempo}</td>
                            <td>${status}</td>
                        </tr>
                    `;
                });
                
                html += `
                                    </tbody>
                                </table>
                            </div>
                        </div>
                    </div>
                `;
                
                document.getElementById('modalFuncionarioTitle').textContent = `Detalhes: ${funcionario.nome || id}`;
                document.getElementById('modalFuncionarioBody').innerHTML = html;
                
                const modal = new bootstrap.Modal(document.getElementById('modalFuncionario'));
                modal.show();
            });
        }
        
        // Busca carregamento em andamento de um funcionário
        function buscarCarregamentoEmAndamento(funcionarioId) {
            carregamentosRef.orderByChild('funcionarioId').equalTo(funcionarioId).once('value', (snapshot) => {
                const carregamentos = snapshot.val() || {};
                const carregamentoEmAndamento = Object.values(carregamentos).find(c => c.inicio && !c.finalizado);
                
                if (carregamentoEmAndamento) {
                    document.getElementById('placaCaminhao').value = carregamentoEmAndamento.placa || '';
                } else {
                    alert('Nenhum carregamento em andamento encontrado para este funcionário!');
                    document.getElementById('funcionarioId').value = '';
                }
            });
        }
        
        // Atualiza o dashboard em tempo real
        function atualizarDashboard() {
            // Atualiza carregamentos em andamento
            carregamentosRef.orderByChild('finalizado').equalTo(false).on('value', (snapshot) => {
                const carregamentos = snapshot.val() || {};
                carregamentosEmAndamento = carregamentos;
                
                // Atualiza a lista na aba principal
                let html = '';
                Object.keys(carregamentos).forEach(key => {
                    const carregamento = carregamentos[key];
                    const tempoDecorrido = Math.floor((new Date().getTime() - carregamento.inicio) / 60000); // em minutos
                    
                    // Define a classe com base no tempo decorrido
                    let tempoClass = 'time-normal';
                    if (tempoDecorrido > 90) tempoClass = 'time-critical';
                    else if (tempoDecorrido > 60) tempoClass = 'time-warning';
                    
                    html += `
                        <div class="card card-carregamento em-andamento mb-2">
                            <div class="card-body">
                                <h6 class="card-title">Placa: ${carregamento.placa || 'N/A'}</h6>
                                <p class="card-text">Funcionário: ${carregamento.funcionarioId}</p>
                                <p class="card-text ${tempoClass}">Tempo: ${tempoDecorrido} minutos</p>
                                <p class="card-text">Início: ${new Date(carregamento.inicio).toLocaleTimeString()}</p>
                            </div>
                        </div>
                    `;
                });
                
                document.getElementById('carregamentosAndamento').innerHTML = html || '<p>Nenhum carregamento em andamento no momento.</p>';
                
                // Atualiza o dashboard
                let dashboardHtml = '';
                Object.keys(carregamentos).forEach(key => {
                    const carregamento = carregamentos[key];
                    const tempoDecorrido = Math.floor((new Date().getTime() - carregamento.inicio) / 60000); // em minutos
                    
                    // Calcula a porcentagem para a barra de progresso (2 horas = 100%)
                    const porcentagem = Math.min(100, (tempoDecorrido / 120) * 100);
                    
                    // Define a cor com base no tempo
                    let progressClass = 'bg-success';
                    if (porcentagem > 75) progressClass = 'bg-warning';
                    if (porcentagem > 90) progressClass = 'bg-danger';
                    
                    dashboardHtml += `
                        <div class="card mb-3">
                            <div class="card-body">
                                <h6 class="card-title">${carregamento.placa || 'N/A'}</h6>
                                <p class="card-text">Funcionário: ${carregamento.funcionarioId}</p>
                                <div class="progress">
                                    <div class="progress-bar ${progressClass} progress-bar-striped progress-bar-animated" 
                                         role="progressbar" style="width: ${porcentagem}%"></div>
                                </div>
                                <p class="card-text mt-2">${tempoDecorrido} minutos (Início: ${new Date(carregamento.inicio).toLocaleTimeString()})</p>
                            </div>
                        </div>
                    `;
                });
                
                document.getElementById('dashboardCarregamentos').innerHTML = dashboardHtml || '<p>Nenhum carregamento em andamento no momento.</p>';
            });
            
            // Atualiza estatísticas do dia
            const hoje = new Date().toISOString().split('T')[0];
            estatisticasRef.child(hoje).once('value', (snapshot) => {
                const dados = snapshot.val() || { total: 0 };
                document.getElementById('totalCarregamentosHoje').textContent = dados.total;
            });
            
            // Atualiza funcionários em ação no dashboard
            funcionariosRef.once('value', (snapshot) => {
                const funcionarios = snapshot.val() || {};
                let funcionariosHtml = '';
                
                Object.keys(funcionarios).forEach(id => {
                    const funcionario = funcionarios[id];
                    
                    // Verifica se o funcionário tem carregamento em andamento
                    const emAcao = Object.values(carregamentosEmAndamento).some(c => c.funcionarioId === id);
                    
                    if (emAcao) {
                        funcionariosHtml += `
                            <div class="card mb-3">
                                <div class="card-body">
                                    <h6 class="card-title">${id} - ${funcionario.nome || 'Nome não informado'}</h6>
                                    <p class="card-text">Cargo: ${funcionario.cargo || 'Não informado'}</p>
                                    <span class="badge bg-success">Em carregamento</span>
                                </div>
                            </div>
                        `;
                    }
                });
                
                document.getElementById('dashboardFuncionarios').innerHTML = funcionariosHtml || '<p>Nenhum funcionário em ação no momento.</p>';
            });
        }
        
        // Atualiza o histórico com filtros
        function atualizarHistorico() {
            const mes = document.getElementById('filtroMes').value;
            const ano = document.getElementById('filtroAno').value;
            const funcionarioId = document.getElementById('filtroFuncionario').value.trim();
            
            // Cria uma data de início e fim para o mês selecionado
            const dataInicio = new Date(`${ano}-${mes}-01`);
            const dataFim = new Date(dataInicio);
            dataFim.setMonth(dataFim.getMonth() + 1);
            
            // Consulta os carregamentos finalizados no período
            carregamentosRef.orderByChild('fim').startAt(dataInicio.getTime()).endAt(dataFim.getTime()).once('value', (snapshot) => {
                const carregamentos = snapshot.val() || {};
                let carregamentosArray = Object.values(carregamentos).filter(c => c.finalizado);
                
                // Filtra por funcionário se especificado
                if (funcionarioId) {
                    carregamentosArray = carregamentosArray.filter(c => c.funcionarioId === funcionarioId);
                }
                
                // Ordena por data de fim (mais recente primeiro)
                carregamentosArray.sort((a, b) => b.fim - a.fim);
                
                // Atualiza a tabela de histórico
                let tabelaHtml = '';
                carregamentosArray.forEach(carregamento => {
                    const inicio = new Date(carregamento.inicio);
                    const fim = new Date(carregamento.fim);
                    const tempo = ((fim - inicio) / 60000).toFixed(2);
                    
                    tabelaHtml += `
                        <tr>
                            <td>${inicio.toLocaleDateString()}</td>
                            <td>${carregamento.placa || 'N/A'}</td>
                            <td>${carregamento.funcionarioId}</td>
                            <td>${inicio.toLocaleTimeString()}</td>
                            <td>${fim.toLocaleTimeString()}</td>
                            <td>${tempo} min</td>
                        </tr>
                    `;
                });
                
                document.getElementById('tabelaHistorico').innerHTML = tabelaHtml || '<tr><td colspan="6">Nenhum carregamento encontrado no período.</td></tr>';
                
                // Calcula estatísticas
                const totalCaminhoes = carregamentosArray.length;
                const valorTotal = totalCaminhoes * 2.5;
                
                let tempoTotal = 0;
                carregamentosArray.forEach(c => {
                    tempoTotal += (c.fim - c.inicio) / 60000;
                });
                
                const mediaTempo = totalCaminhoes > 0 ? (tempoTotal / totalCaminhoes).toFixed(2) : 0;
                
                // Atualiza os cards de estatísticas
                document.getElementById('totalCaminhoes').textContent = totalCaminhoes;
                document.getElementById('mediaTempo').textContent = `${mediaTempo} min`;
                document.getElementById('valorTotal').textContent = `R$ ${valorTotal.toFixed(2)}`;
                
                // Calcula os top funcionários
                const funcionariosMap = {};
                carregamentosArray.forEach(c => {
                    if (!funcionariosMap[c.funcionarioId]) {
                        funcionariosMap[c.funcionarioId] = {
                            count: 0,
                            tempoTotal: 0,
                            nome: 'Desconhecido'
                        };
                    }
                    
                    funcionariosMap[c.funcionarioId].count++;
                    funcionariosMap[c.funcionarioId].tempoTotal += (c.fim - c.inicio) / 60000;
                });
                
                // Busca os nomes dos funcionários
                const promises = Object.keys(funcionariosMap).map(id => {
                    return funcionariosRef.child(id).once('value').then(snap => {
                        if (snap.exists()) {
                            funcionariosMap[id].nome = snap.val().nome || 'Desconhecido';
                        }
                    });
                });
                
                Promise.all(promises).then(() => {
                    // Converte o mapa para array e ordena
                    const topFuncionarios = Object.keys(funcionariosMap).map(id => {
                        return {
                            id,
                            nome: funcionariosMap[id].nome,
                            count: funcionariosMap[id].count,
                            tempoMedio: (funcionariosMap[id].tempoTotal / funcionariosMap[id].count).toFixed(2),
                            valor: funcionariosMap[id].count * 2.5
                        };
                    }).sort((a, b) => b.count - a.count);
                    
                    // Atualiza a tabela de top funcionários
                    let topHtml = '';
                    topFuncionarios.forEach((func, index) => {
                        topHtml += `
                            <tr>
                                <td>${index + 1}</td>
                                <td>${func.nome} (${func.id})</td>
                                <td>${func.count}</td>
                                <td>${func.tempoMedio} min</td>
                                <td>R$ ${func.valor.toFixed(2)}</td>
                            </tr>
                        `;
                    });
                    
                    document.getElementById('topFuncionarios').innerHTML = topHtml || '<tr><td colspan="5">Nenhum dado disponível</td></tr>';
                });
            });
        }

        // Event Listeners
        document.addEventListener('DOMContentLoaded', function() {
            // Inicializa o dashboard
            atualizarDashboard();
            
            // Atualiza o dashboard a cada minuto
            setInterval(atualizarDashboard, 60000);
            
            // Carrega o histórico com os valores atuais
            const hoje = new Date();
            document.getElementById('filtroMes').value = (hoje.getMonth() + 1).toString().padStart(2, '0');
            document.getElementById('filtroAno').value = hoje.getFullYear().toString();
            atualizarHistorico();
            
            // Operação: Iniciar Carregamento
            document.getElementById('btnIniciarCarregamento').addEventListener('click', function() {
                operacaoAtual = 'iniciar';
                document.getElementById('formTitle').textContent = 'Iniciar Carregamento';
                document.getElementById('formContainer').style.display = 'block';
                document.getElementById('placaCaminhao').value = '';
                document.getElementById('funcionarioId').value = '';
                document.getElementById('funcionarioId').focus();
            });
            
            // Operação: Finalizar Carregamento
            document.getElementById('btnFinalizarCarregamento').addEventListener('click', function() {
                operacaoAtual = 'finalizar';
                document.getElementById('formTitle').textContent = 'Finalizar Carregamento';
                document.getElementById('formContainer').style.display = 'block';
                document.getElementById('placaCaminhao').value = '';
                document.getElementById('funcionarioId').value = '';
                document.getElementById('funcionarioId').focus();
            });
            
            // Confirmar operação
            document.getElementById('btnConfirmar').addEventListener('click', function() {
                const funcionarioId = document.getElementById('funcionarioId').value.trim();
                const placa = document.getElementById('placaCaminhao').value.trim().toUpperCase();
                
                if (!funcionarioId) {
                    alert('Por favor, informe o código do funcionário!');
                    return;
                }
                
                if (!funcionarioId.startsWith('GZL-EO-')) {
                    alert('Código de funcionário inválido! Deve começar com GZL-EO-');
                    return;
                }
                
                if (!placa) {
                    alert('Por favor, informe a placa do caminhão!');
                    return;
                }
                
                if (operacaoAtual === 'iniciar') {
                    // Verifica se o funcionário já tem um carregamento em andamento
                    carregamentosRef.orderByChild('funcionarioId').equalTo(funcionarioId).once('value', (snapshot) => {
                        const carregamentos = snapshot.val() || {};
                        const carregamentoEmAndamento = Object.values(carregamentos).find(c => c.inicio && !c.finalizado);
                        
                        if (carregamentoEmAndamento) {
                            alert('Este funcionário já tem um carregamento em andamento!');
                            return;
                        }
                        
                        // Verifica se o funcionário existe
                        funcionariosRef.child(funcionarioId).once('value', (snap) => {
                            if (!snap.exists()) {
                                alert('Funcionário não encontrado! Verifique o código.');
                                return;
                            }
                            
                            // Cria novo carregamento
                            const novoCarregamento = {
                                funcionarioId,
                                placa,
                                inicio: new Date().getTime(),
                                finalizado: false
                            };
                            
                            const novoRef = carregamentosRef.push();
                            novoRef.set(novoCarregamento)
                                .then(() => {
                                    alert('Carregamento iniciado com sucesso!');
                                    document.getElementById('formContainer').style.display = 'none';
                                    operacaoAtual = null;
                                    atualizarDashboard();
                                })
                                .catch(error => {
                                    console.error('Erro ao iniciar carregamento:', error);
                                    alert('Erro ao iniciar carregamento!');
                                });
                        });
                    });
                } else if (operacaoAtual === 'finalizar') {
                    // Finaliza o carregamento
                    carregamentosRef.orderByChild('funcionarioId').equalTo(funcionarioId).once('value', (snapshot) => {
                        const carregamentos = snapshot.val() || {};
                        const carregamentoEmAndamento = Object.entries(carregamentos).find(([key, c]) => c.inicio && !c.finalizado);
                        
                        if (!carregamentoEmAndamento) {
                            alert('Nenhum carregamento em andamento encontrado para este funcionário!');
                            return;
                        }
                        
                        const [key, carregamento] = carregamentoEmAndamento;
                        
                        // Atualiza o carregamento
                        const updates = {
                            fim: new Date().getTime(),
                            finalizado: true,
                            placa: placa || carregamento.placa
                        };
                        
                        carregamentosRef.child(key).update(updates)
                            .then(() => {
                                // Atualiza estatísticas do dia
                                const hoje = new Date().toISOString().split('T')[0];
                                estatisticasRef.child(hoje).transaction((currentData) => {
                                    if (currentData === null) {
                                        return { total: 1 };
                                    }
                                    currentData.total = (currentData.total || 0) + 1;
                                    return currentData;
                                });
                                
                                alert('Carregamento finalizado com sucesso!');
                                document.getElementById('formContainer').style.display = 'none';
                                operacaoAtual = null;
                                atualizarDashboard();
                                atualizarHistorico();
                            })
                            .catch(error => {
                                console.error('Erro ao finalizar carregamento:', error);
                                alert('Erro ao finalizar carregamento!');
                            });
                    });
                }
            });
            
            // Cancelar operação
            document.getElementById('btnCancelar').addEventListener('click', function() {
                document.getElementById('formContainer').style.display = 'none';
                operacaoAtual = null;
            });
            
            // Cadastrar Funcionário
            document.getElementById('btnCadastrar').addEventListener('click', function() {
                const nome = document.getElementById('novoNome').value.trim();
                const cargo = document.getElementById('novoCargo').value.trim();
                
                if (!nome || !cargo) {
                    alert('Por favor, preencha todos os campos!');
                    return;
                }
                
                const codigo = gerarCodigoFuncionario();
                const funcionario = {
                    nome,
                    cargo,
                    dataCadastro: new Date().getTime()
                };
                
                funcionariosRef.child(codigo).set(funcionario)
                    .then(() => {
                        // Mostra o código gerado
                        document.getElementById('codigoGerado').textContent = codigo;
                        document.getElementById('codigoGerado').style.display = 'block';
                        
                        document.getElementById('infoCadastro').innerHTML = `
                            <p><strong>Nome:</strong> ${nome}</p>
                            <p><strong>Cargo:</strong> ${cargo}</p>
                            <p><strong>Data de Cadastro:</strong> ${new Date().toLocaleDateString()}</p>
                        `;
                        
                        // Habilita o botão de download
                        document.getElementById('btnDownloadPDF').style.display = 'block';
                        document.getElementById('btnDownloadPDF').onclick = function() {
                            gerarPDFCodigo(codigo, nome, cargo);
                        };
                        
                        // Limpa os campos
                        document.getElementById('novoNome').value = '';
                        document.getElementById('novoCargo').value = '';
                    })
                    .catch(error => {
                        console.error('Erro ao cadastrar funcionário:', error);
                        alert('Erro ao cadastrar funcionário!');
                    });
            });
            
            // Buscar Funcionário
            document.getElementById('btnBuscar').addEventListener('click', function() {
                const codigo = document.getElementById('buscarFuncionario').value.trim();
                if (!codigo) {
                    alert('Por favor, informe o código do funcionário!');
                    return;
                }
                
                if (!codigo.startsWith('GZL-EO-')) {
                    alert('Código de funcionário inválido! Deve começar com GZL-EO-');
                    return;
                }
                
                buscarFuncionario(codigo, true);
            });
            
            // Filtro de histórico
            document.getElementById('btnFiltrar').addEventListener('click', function() {
                atualizarHistorico();
            });
        });
    </script>
</body>
</html>