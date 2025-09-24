class EmpresaPrivada:

    def __init__(self, nome, risco, equilibrio_financeiro):

        self.nome = nome

        self.risco = risco  # valor entre 0 (baixo) e 1 (alto)

        self.equilibrio_financeiro = equilibrio_financeiro  # valor entre 0 (desequilibrada) e 1 (equilibrada)



    def esta_segura_para_investir(self):

        if self.risco <= 0.4 and self.equilibrio_financeiro >= 0.6:

            return True

        return False



    def resumo_avaliacao(self):

        status = "Segura para investir" if self.esta_segura_para_investir() else "Alto risco ou desequilíbrio financeiro"

        return f"Empresa: {self.nome}\nRisco: {self.risco}\nEquilíbrio Financeiro: {self.equilibrio_financeiro}\nStatus: {status}"

