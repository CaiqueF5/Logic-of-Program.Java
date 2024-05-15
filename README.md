public static void main(String[] args) {
			int[] vet=new int[5];
			preenche(vet);
			mostra(vet);
			bubbleSort(vet);
			mostra(vet);

		}
		
		public static void preenche(int[] v) {
			Random rand=new Random();
			
			for(int i=0; i<v.length;i++) {
				v[i]=rand.nextInt(10);
			}
		}
		
		public static void mostra(int[] v) {
			for(int i=0; i<v.length; i++) {
				System.out.print(v[i]+" ");
			}
			System.out.println();
		}
		
		public static void bubbleSort(int[] v) {
			boolean trocou=true;
			int aux;
			while(trocou) {
				trocou=false;
				for(int i=0; i<v.length-1; i++) {
					if(v[i]>v[i+1]) {
						aux=v[i];
						v[i]=v[i+1];
						v[i+1]=aux;
						trocou=true;
					}
				}
			}
		}
