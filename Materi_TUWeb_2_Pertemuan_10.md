# 📚 Materi TUWeb 2 – Pertemuan 10  
## 🚀 Pengenalan Vue.js dan Data Binding - **Learning by Doing**  
**Studi Kasus: Aplikasi Stok Bahan Ajar SITTA dengan Vue.js**

---

## 🎯 **Tujuan Pembelajaran Komprehensif**

### 📋 **Kompetensi Utama**
Setelah mengikuti pertemuan ini, mahasiswa diharapkan mampu:

#### 🧠 **Kognitif (Pengetahuan)**
- **C2 (Memahami)**: Konsep dasar Vue.js framework dan arsitektur MVVM
- **C3 (Menerapkan)**: Data binding (one-way dan two-way) dalam aplikasi nyata
- **C4 (Menganalisis)**: Perbedaan computed properties vs methods vs watchers
- **C5 (Mengevaluasi)**: Performa dan best practices dalam pengembangan Vue.js

#### 🛠️ **Psikomotorik (Keterampilan)**
- **Setup Environment**: Menginstal dan mengkonfigurasi Vue.js development environment
- **Component Creation**: Membuat Vue components dengan proper structure
- **Data Manipulation**: Implementasi berbagai teknik data binding
- **Debugging**: Mengidentifikasi dan memperbaiki error dalam Vue.js applications
- **Performance Optimization**: Menerapkan teknik optimasi untuk aplikasi Vue.js

#### 💝 **Afektif (Sikap)**
- **Problem Solving**: Berpikir kritis dalam memecahkan masalah UI/UX
- **Code Quality**: Menulis kode yang clean, maintainable, dan documented
- **Collaboration**: Memahami importance of code organization untuk team work
- **Continuous Learning**: Mengembangkan mindset untuk belajar teknologi baru

---

## ⏰ **Timeline Pembelajaran**

| **Waktu** | **Aktivitas** | **Fokus** | **Output** |
|-----------|---------------|-----------|------------|
| **09:00-09:30** | **Konsep Vue.js Fundamentals** | Teori & Demo | Pemahaman arsitektur Vue.js |
| **09:30-10:15** | **Data Binding Deep Dive** | Praktik | One-way & two-way binding implementation |
| **10:15-10:30** | **Coffee Break** | - | Refresh & networking |
| **10:30-11:15** | **Conditional Rendering** | Praktik | Dynamic UI dengan v-if & v-show |
| **11:15-12:00** | **Computed & Methods** | Praktik | Optimasi data processing |
| **12:00-13:00** | **Ishoma** | - | Lunch break |
| **13:00-13:45** | **Watchers & Reactivity** | Praktik | Advanced reactivity patterns |
| **13:45-14:30** | **SITTA Case Study** | Proyek | Aplikasi stok bahan ajar |
| **14:30-15:00** | **Review & Q&A** | Diskusi | Best practices & troubleshooting |

---

## 🏗️ **Struktur Pembelajaran**

### 📚 **Materi Teori (40%)**
1. **Vue.js Fundamentals** - Architecture & concepts
2. **Reactivity System** - How Vue.js handles data changes
3. **Component Lifecycle** - From creation to destruction
4. **Performance Patterns** - Best practices & optimization

### 💻 **Praktik Terstruktur (60%)**
1. **Hands-on Labs** - Step-by-step implementation
2. **Code-along Sessions** - Real-time coding with instructor
3. **Pair Programming** - Collaborative problem solving
4. **Project Development** - Complete SITTA stock application

---

## 🎯 **Learning Outcomes Detail**

### 🔰 **Level 1: Foundation (Beginner)**
- ✅ Setup Vue.js development environment
- ✅ Create basic Vue instance dengan data dan methods
- ✅ Implement one-way data binding dengan mustaches
- ✅ Use two-way data binding dengan v-model
- ✅ Apply conditional rendering dengan v-if/v-show

### 🚀 **Level 2: Intermediate (Competent)**
- ✅ Master computed properties untuk data transformation
- ✅ Implement watchers untuk side effects
- ✅ Handle complex form interactions
- ✅ Optimize performance dengan proper reactivity usage
- ✅ Debug common Vue.js issues

### 🏆 **Level 3: Advanced (Proficient)**
- ✅ Design scalable Vue.js architecture
- ✅ Implement custom directives dan filters
- ✅ Handle async operations dengan proper error handling
- ✅ Optimize large-scale applications
- ✅ Contribute to Vue.js ecosystem best practices

---

## 📖 **Materi 1: Konsep Dasar Vue.js - **Deep Dive**

### 🎯 **Apa itu Vue.js?**

**📖 Definisi:** Vue.js (dibaca "view") adalah JavaScript framework progresif untuk membangun user interfaces. Vue dirancang dari ground up untuk menjadi approachable dan incrementally adoptable.

**🌟 Core Philosophy:**
- **🔄 Progressive Enhancement**: Mulai dari small features hingga full SPA
- **🎯 Approachable API**: Mudah dipelajari untuk pemula
- **⚡ High Performance**: Virtual DOM dan optimized reactivity system
- **🛠️ Versatile**: Bisa digunakan untuk berbagai use cases
- **📱 Component-Based**: Reusable UI components
- **🔧 Tooling Friendly**: Integrasi baik dengan modern tooling

### 🏗️ **Arsitektur Vue.js - MVVM Pattern**

```
┌─────────────────────────────────────────────────────────────┐
│                    Vue.js Application                      │
├─────────────────────────────────────────────────────────────┤
│  📱 View Layer (Template)                                  │
│  ├── HTML Templates dengan Vue Directives                   │
│  ├── Data Binding {{ }}                                     │
│  └── Event Handling @click                                 │
├─────────────────────────────────────────────────────────────┤
│  🧠 ViewModel Layer (Vue Instance)                         │
│  ├── Data Properties                                        │
│  ├── Computed Properties                                    │
│  ├── Methods                                                │
│  └── Watchers                                               │
├─────────────────────────────────────────────────────────────┤
│  💾 Model Layer (Data/State)                               │
│  ├── API Responses                                          │
│  ├── Local Storage                                          │
│  └── Application State                                     │
└─────────────────────────────────────────────────────────────┘
```

### 🔧 **Vue Instance Anatomy - Complete Structure**

```javascript
// 🏗️ Struktur lengkap Vue instance dengan semua options
const app = new Vue({
    // 🎯 Elemen target untuk mounting
    el: '#app',
    
    // 📊 Data - Reactive state
    data: {
        // Primitive values
        message: 'Hello Vue.js!',
        count: 0,
        isVisible: true,
        
        // Objects
        user: {
            id: 1,
            name: 'Ahmad Rizki',
            email: 'ahmad@ut.ac.id',
            profile: {
                avatar: 'avatar.jpg',
                role: 'student'
            }
        },
        
        // Arrays
        items: [
            { id: 1, name: 'Buku A', stock: 10 },
            { id: 2, name: 'Buku B', stock: 5 }
        ],
        
        // Computed-ready data
        filters: {
            search: '',
            category: 'all',
            sortBy: 'name'
        }
    },
    
    // 🧮 Computed Properties - Cached calculations
    computed: {
        // Basic computed property
        doubleCount() {
            return this.count * 2;
        },
        
        // Computed dengan dependencies
        fullName() {
            return `${this.user.profile.role}: ${this.user.name}`;
        },
        
        // Computed dengan array filtering
        filteredItems() {
            return this.items.filter(item => 
                item.name.toLowerCase().includes(this.filters.search.toLowerCase())
            );
        },
        
        // Computed dengan conditional logic
        stockStatus() {
            const totalStock = this.items.reduce((sum, item) => sum + item.stock, 0);
            if (totalStock === 0) return 'empty';
            if (totalStock < 10) return 'low';
            return 'available';
        },
        
        // Getter-only computed
        userInfo() {
            return {
                displayName: this.user.name.toUpperCase(),
                domain: this.user.email.split('@')[1],
                isPremium: this.user.profile.role === 'admin'
            };
        }
    },
    
    // 🔧 Methods - Functions untuk actions
    methods: {
        // Basic method
        increment() {
            this.count++;
        },
        
        // Method dengan parameters
        addItem(item) {
            this.items.push({
                id: Date.now(),
                name: item.name,
                stock: item.stock || 0
            });
        },
        
        // Method dengan validation
        updateStock(itemId, newStock) {
            if (newStock < 0) {
                alert('Stock tidak boleh negatif!');
                return;
            }
            
            const item = this.items.find(i => i.id === itemId);
            if (item) {
                item.stock = newStock;
            }
        },
        
        // Async method
        async fetchUserData() {
            try {
                this.isLoading = true;
                const response = await fetch('/api/user');
                const data = await response.json();
                this.user = { ...this.user, ...data };
            } catch (error) {
                console.error('Error fetching user:', error);
                this.error = 'Gagal memuat data user';
            } finally {
                this.isLoading = false;
            }
        },
        
        // Event handler method
        handleFormSubmit(event) {
            event.preventDefault();
            // Process form data
            this.saveData();
        }
    },
    
    // 👁️ Watchers - React to data changes
    watch: {
        // Simple watcher
        count(newVal, oldVal) {
            console.log(`Count changed from ${oldVal} to ${newVal}`);
            
            // Trigger action when count reaches certain value
            if (newVal === 10) {
                this.celebrate();
            }
        },
        
        // Deep watcher for objects
        user: {
            handler(newUser, oldUser) {
                console.log('User data changed:', newUser);
                this.saveUserToStorage();
            },
            deep: true // Watch nested properties
        },
        
        // Immediate watcher
        'filters.search': {
            handler(newSearch) {
                this.debounceSearch();
            },
            immediate: true // Run immediately on component creation
        },
        
        // Array watcher
        items: {
            handler(newItems, oldItems) {
                this.updateTotalStock();
            },
            deep: true
        }
    },
    
    // 🎭 Lifecycle Hooks
    beforeCreate() {
        console.log('🔴 beforeCreate: Instance initialized');
    },
    
    created() {
        console.log('🟡 created: Instance created, data available');
        // Good for API calls
        this.fetchInitialData();
    },
    
    beforeMount() {
        console.log('🟠 beforeMount: Template compiled, not mounted yet');
    },
    
    mounted() {
        console.log('🟢 mounted: Component mounted to DOM');
        // Good for DOM manipulation, third-party libraries
        this.initializePlugins();
    },
    
    beforeUpdate() {
        console.log('🔵 beforeUpdate: Data changed, DOM will update');
    },
    
    updated() {
        console.log('🟣 updated: DOM updated');
    },
    
    beforeDestroy() {
        console.log('⚫ beforeDestroy: Cleanup before destruction');
        this.cleanup();
    },
    
    destroyed() {
        console.log('⚪ destroyed: Component destroyed');
    },
    
    // 🎨 Template-specific options
    template: `<!-- Optional template string -->`,
    
    // 🔌 Components registration
    components: {
        'my-component': MyComponent
    },
    
    // 🎭 Directives
    directives: {
        focus: {
            inserted: function (el) {
                el.focus();
            }
        }
    },
    
    // 🎨 Filters (Vue 2)
    filters: {
        capitalize(value) {
            if (!value) return '';
            return value.charAt(0).toUpperCase() + value.slice(1);
        }
    }
});
```

### 📝 **Praktik 1: Vue.js Setup - Development Environment**

#### **🛠️ Setup Options**

**Option 1: CDN (Quick Start)**
```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vue.js Quick Start - SITTA</title>
    
    <!-- Vue.js 2 CDN -->
    <script src="https://cdn.jsdelivr.net/npm/vue@2.6.14/dist/vue.js"></script>
    
    <!-- Bootstrap untuk styling -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet">
    
    <!-- Custom CSS -->
    <style>
        .vue-app {
            max-width: 800px;
            margin: 2rem auto;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }
        
        .status-badge {
            display: inline-block;
            padding: 0.25rem 0.5rem;
            border-radius: 0.25rem;
            font-size: 0.875rem;
            font-weight: 600;
        }
        
        .status-available { background-color: #d4edda; color: #155724; }
        .status-low { background-color: #fff3cd; color: #856404; }
        .status-empty { background-color: #f8d7da; color: #721c24; }
        
        .fade-enter-active, .fade-leave-active {
            transition: opacity 0.5s;
        }
        
        .fade-enter, .fade-leave-to {
            opacity: 0;
        }
    </style>
</head>
<body>
    <div class="container">
        <div id="app" class="vue-app">
            <!-- Header dengan dynamic message -->
            <header class="text-center mb-4">
                <h1 class="display-4">
                    🎓 {{ appTitle }}
                </h1>
                <p class="lead">{{ appDescription }}</p>
                <div class="badge bg-primary">{{ currentDateTime }}</div>
            </header>
            
            <!-- User Info Section -->
            <section class="card mb-4" v-if="user.isLoggedIn">
                <div class="card-header">
                    <h5 class="mb-0">👤 Informasi User</h5>
                </div>
                <div class="card-body">
                    <div class="row">
                        <div class="col-md-6">
                            <p><strong>Nama:</strong> {{ user.name }}</p>
                            <p><strong>Email:</strong> {{ user.email }}</p>
                        </div>
                        <div class="col-md-6">
                            <p><strong>Role:</strong> 
                                <span class="status-badge" :class="userRoleClass">
                                    {{ user.role }}
                                </span>
                            </p>
                            <p><strong>Status:</strong> 
                                <span class="status-badge" :class="userStatusClass">
                                    {{ user.status }}
                                </span>
                            </p>
                        </div>
                    </div>
                </div>
            </section>
            
            <!-- Counter Demo -->
            <section class="card mb-4">
                <div class="card-header">
                    <h5 class="mb-0">🔢 Counter Demo</h5>
                </div>
                <div class="card-body text-center">
                    <h2 class="display-2">{{ count }}</h2>
                    <p class="text-muted">Double Count: {{ doubleCount }}</p>
                    <div class="btn-group" role="group">
                        <button @click="decrement" class="btn btn-outline-primary">➖</button>
                        <button @click="increment" class="btn btn-primary">➕</button>
                        <button @click="reset" class="btn btn-outline-secondary">🔄 Reset</button>
                    </div>
                </div>
            </section>
            
            <!-- Stock Overview -->
            <section class="card mb-4">
                <div class="card-header">
                    <h5 class="mb-0">📦 Stock Overview</h5>
                </div>
                <div class="card-body">
                    <div class="row text-center">
                        <div class="col-md-4">
                            <h4 class="text-primary">{{ totalItems }}</h4>
                            <p class="text-muted">Total Items</p>
                        </div>
                        <div class="col-md-4">
                            <h4 class="text-success">{{ totalStock }}</h4>
                            <p class="text-muted">Total Stock</p>
                        </div>
                        <div class="col-md-4">
                            <h4 class="text-info">{{ lowStockItems }}</h4>
                            <p class="text-muted">Low Stock Items</p>
                        </div>
                    </div>
                    
                    <!-- Stock Status -->
                    <div class="mt-3 text-center">
                        <span class="status-badge" :class="stockStatusClass">
                            {{ stockStatusMessage }}
                        </span>
                    </div>
                </div>
            </section>
            
            <!-- Interactive Features -->
            <section class="card">
                <div class="card-header">
                    <h5 class="mb-0">🎮 Interactive Features</h5>
                </div>
                <div class="card-body">
                    <div class="row">
                        <div class="col-md-6">
                            <div class="form-group mb-3">
                                <label for="messageInput">Pesan:</label>
                                <input 
                                    id="messageInput"
                                    v-model="message" 
                                    class="form-control"
                                    placeholder="Ketik pesan..."
                                    @keyup.enter="sendMessage"
                                >
                            </div>
                            <button @click="sendMessage" class="btn btn-success w-100">
                                📤 Kirim Pesan
                            </button>
                        </div>
                        <div class="col-md-6">
                            <div class="form-group mb-3">
                                <label>Toggle Features:</label>
                                <div class="form-check">
                                    <input 
                                        v-model="features.showNotifications" 
                                        type="checkbox" 
                                        class="form-check-input"
                                        id="notifications"
                                    >
                                    <label class="form-check-label" for="notifications">
                                        Show Notifications
                                    </label>
                                </div>
                                <div class="form-check">
                                    <input 
                                        v-model="features.enableDarkMode" 
                                        type="checkbox" 
                                        class="form-check-input"
                                        id="darkmode"
                                    >
                                    <label class="form-check-label" for="darkmode">
                                        Enable Dark Mode
                                    </label>
                                </div>
                            </div>
                        </div>
                    </div>
                    
                    <!-- Message Display -->
                    <transition name="fade">
                        <div v-if="message" class="alert alert-info mt-3">
                            <strong>Pesan:</strong> {{ message }}
                        </div>
                    </transition>
                </div>
            </section>
        </div>
    </div>

    <script>
        // 🚀 Vue Instance Creation
        new Vue({
            el: '#app',
            
            // 📊 Data Properties
            data: {
                appTitle: 'SITTA - Vue.js Demo',
                appDescription: 'Sistem Informasi Terintegrasi Tutorial & Assessment',
                count: 0,
                message: '',
                
                // User data
                user: {
                    isLoggedIn: true,
                    name: 'Ahmad Rizki',
                    email: 'ahmad.rizki@ut.ac.id',
                    role: 'student',
                    status: 'active'
                },
                
                // Features
                features: {
                    showNotifications: true,
                    enableDarkMode: false
                },
                
                // Sample stock data
                stockItems: [
                    { id: 1, name: 'Buku Pemrograman Web', stock: 15 },
                    { id: 2, name: 'Buku Database', stock: 3 },
                    { id: 3, name: 'Buku Algoritma', stock: 0 },
                    { id: 4, name: 'Buku Jaringan', stock: 8 }
                ]
            },
            
            // 🧮 Computed Properties
            computed: {
                doubleCount() {
                    return this.count * 2;
                },
                
                currentDateTime() {
                    return new Date().toLocaleString('id-ID');
                },
                
                userRoleClass() {
                    const classes = {
                        'admin': 'status-available',
                        'teacher': 'status-low',
                        'student': 'status-empty'
                    };
                    return classes[this.user.role] || 'status-empty';
                },
                
                userStatusClass() {
                    return this.user.status === 'active' ? 'status-available' : 'status-empty';
                },
                
                totalItems() {
                    return this.stockItems.length;
                },
                
                totalStock() {
                    return this.stockItems.reduce((sum, item) => sum + item.stock, 0);
                },
                
                lowStockItems() {
                    return this.stockItems.filter(item => item.stock < 5).length;
                },
                
                stockStatusClass() {
                    if (this.totalStock === 0) return 'status-empty';
                    if (this.lowStockItems > 0) return 'status-low';
                    return 'status-available';
                },
                
                stockStatusMessage() {
                    if (this.totalStock === 0) return 'Stok Habis';
                    if (this.lowStockItems > 0) return `${this.lowStockItems} Item Stok Rendah`;
                    return 'Stok Aman';
                }
            },
            
            // 🔧 Methods
            methods: {
                increment() {
                    this.count++;
                    this.showNotification('Counter increased!');
                },
                
                decrement() {
                    if (this.count > 0) {
                        this.count--;
                        this.showNotification('Counter decreased!');
                    }
                },
                
                reset() {
                    this.count = 0;
                    this.showNotification('Counter reset!');
                },
                
                sendMessage() {
                    if (this.message.trim()) {
                        this.showNotification(`Pesan terkirim: ${this.message}`);
                        this.message = '';
                    }
                },
                
                showNotification(message) {
                    if (this.features.showNotifications) {
                        // Create toast notification
                        console.log('🔔 Notification:', message);
                    }
                }
            },
            
            // 👁️ Watchers
            watch: {
                count(newVal) {
                    if (newVal === 10) {
                        this.showNotification('🎉 Count reached 10!');
                    }
                },
                
                'features.enableDarkMode'(newVal) {
                    document.body.classList.toggle('dark-mode', newVal);
                }
            },
            
            // 🎭 Lifecycle Hooks
            mounted() {
                console.log('🚀 Vue app mounted successfully!');
                this.showNotification('Selamat datang di Vue.js Demo!');
            }
        });
    </script>
</body>
</html>
```

#### **Option 2: Vue CLI (Production Ready)**
```bash
# Install Vue CLI globally
npm install -g @vue/cli

# Create new Vue project
vue create sitta-vue-app

# Navigate to project
cd sitta-vue-app

# Start development server
npm run serve
```

#### **Option 3: Vite (Modern & Fast)**
```bash
# Create Vue + Vite project
npm create vue@latest sitta-vue-app

# Navigate and install dependencies
cd sitta-vue-app
npm install

# Start development server
npm run dev
```

### 🎯 **Best Practices dari Awal**

#### **1. Component Structure**
```javascript
// 📁 src/components/StockItem.vue
export default {
    name: 'StockItem',
    
    // Props untuk data dari parent
    props: {
        item: {
            type: Object,
            required: true,
            validator: function(value) {
                return value.id && value.name && value.stock >= 0;
            }
        }
    },
    
    // Data lokal untuk component
    data() {
        return {
            isEditing: false,
            localStock: this.item.stock
        };
    },
    
    // Computed properties
    computed: {
        stockStatus() {
            return this.localStock === 0 ? 'empty' : 
                   this.localStock < 5 ? 'low' : 'available';
        }
    },
    
    // Methods
    methods: {
        updateStock() {
            this.$emit('stock-updated', {
                id: this.item.id,
                newStock: this.localStock
            });
            this.isEditing = false;
        }
    }
};
```

#### **2. State Management Pattern**
```javascript
// 📁 src/store/stock.js
export default {
    state: {
        items: [],
        loading: false,
        error: null
    },
    
    mutations: {
        SET_ITEMS(state, items) {
            state.items = items;
        },
        
        UPDATE_STOCK(state, { id, stock }) {
            const item = state.items.find(item => item.id === id);
            if (item) {
                item.stock = stock;
            }
        }
    },
    
    actions: {
        async fetchItems({ commit }) {
            commit('SET_LOADING', true);
            try {
                const items = await api.fetchStockItems();
                commit('SET_ITEMS', items);
            } catch (error) {
                commit('SET_ERROR', error.message);
            } finally {
                commit('SET_LOADING', false);
            }
        }
    }
};
```

### 🔍 **Vue.js DevTools Setup**

#### **Browser Extension Installation**
1. **Chrome**: Vue.js devtools
2. **Firefox**: Vue.js devtools
3. **Safari**: Vue.js devtools

#### **Features Available**
- 🔍 Component inspection
- 📊 Vuex state management
- ⏡ Performance profiling
- 🐛 Debugging capabilities
- 📱 Time-travel debugging

---

**🎉 Selamat! Anda telah mempelajari fundamental Vue.js dengan comprehensive approach!**

**📝 Next Steps:**
1. Pilih setup method yang sesuai dengan kebutuhan
2. Install Vue.js DevTools untuk debugging
3. Practice dengan contoh kode di atas
4. Siapkan untuk materi berikutnya: **Data Binding Deep Dive**

---

## 🔄 **Materi 2: Data Binding - **Mastering Reactivity**

### 🎯 **Konsep Data Binding**

**📖 Definisi:** Data binding adalah mekanisme untuk sinkronisasi otomatis antara data (JavaScript) dan tampilan (HTML). Vue.js menyediakan sistem reactivity yang powerful dan efficient.

**🌟 Types of Data Binding:**
- **🔄 One-Way Binding**: Data → View (JavaScript ke HTML)
- **🔀 Two-Way Binding**: Data ↔ View (JavaScript ↔ HTML)
- **🎯 Event Binding**: View → Data (HTML ke JavaScript)

---

## 📤 **One-Way Data Binding - Data to View**

### 1️⃣ **Mustache Interpolation {{ }}**

**🎯 Basic Usage:**
```html
<div id="app">
    <!-- Simple text interpolation -->
    <h1>{{ title }}</h1>
    <p>Welcome, {{ user.name }}!</p>
    
    <!-- Expression evaluation -->
    <p>Total: {{ price * quantity }}</p>
    <p>Status: {{ isActive ? 'Active' : 'Inactive' }}</p>
    
    <!-- Method calls -->
    <p>Formatted date: {{ formatDate(currentDate) }}</p>
    
    <!-- Computed properties -->
    <p>Full name: {{ fullName }}</p>
    <p>Cart total: {{ cartTotal | currency }}</p>
</div>

<script>
new Vue({
    el: '#app',
    data: {
        title: 'SITTA Dashboard',
        user: {
            name: 'Ahmad Rizki',
            email: 'ahmad@ut.ac.id'
        },
        price: 50000,
        quantity: 3,
        isActive: true,
        currentDate: new Date()
    },
    computed: {
        fullName() {
            return `${this.user.name} (${this.user.email})`;
        },
        cartTotal() {
            return this.price * this.quantity;
        }
    },
    methods: {
        formatDate(date) {
            return date.toLocaleDateString('id-ID');
        }
    },
    filters: {
        currency(value) {
            return new Intl.NumberFormat('id-ID', {
                style: 'currency',
                currency: 'IDR'
            }).format(value);
        }
    }
});
</script>
```

**⚡ Performance Tips:**
```html
<!-- ✅ GOOD: Simple expressions -->
<p>{{ message }}</p>
<p>{{ count + 1 }}</p>
<p>{{ user.name || 'Anonymous' }}</p>

<!-- ❌ AVOID: Complex expressions in template -->
<!-- Move to computed properties instead -->
<p>{{ items.filter(item => item.active).reduce((sum, item) => sum + item.price, 0) }}</p>

<!-- ✅ BETTER: Use computed property -->
<p>{{ totalActiveItemsPrice }}</p>
```

### 2️⃣ **Directive v-text**

**🎯 Usage:**
```html
<div id="app">
    <!-- v-text updates textContent -->
    <p v-text="message"></p>
    <p v-text="'User: ' + user.name"></p>
    
    <!-- Equivalent to mustache but safer for XSS -->
    <div v-text="userInput"></div>
    
    <!-- Good for dynamic content that should be plain text -->
    <h1 v-text="pageTitle"></h1>
    <p v-text="pageDescription"></p>
</div>

<script>
new Vue({
    el: '#app',
    data: {
        message: 'Hello from v-text!',
        user: { name: 'John Doe' },
        userInput: '<script>alert("XSS")</script>', // Safe with v-text
        pageTitle: 'SITTA Learning Platform',
        pageDescription: 'Interactive learning management system'
    }
});
</script>
```

**🔒 Security Benefits:**
- `v-text` automatically escapes HTML content
- Prevents XSS attacks
- Safer untuk user-generated content

### 3️⃣ **Directive v-html**

**⚠️ SECURITY WARNING:** Use with caution! Only with trusted content.

```html
<div id="app">
    <!-- v-html updates innerHTML -->
    <div v-html="formattedContent"></div>
    
    <!-- Good for trusted, sanitized content -->
    <div v-html="sanitizedUserContent"></div>
    
    <!-- Rich text editor output -->
    <div v-html="editorContent"></div>
</div>

<script>
new Vue({
    el: '#app',
    data: {
        // Trusted content from CMS
        formattedContent: `
            <h2>Welcome to <strong>SITTA</strong></h2>
            <p>Learn <em>web development</em> interactively!</p>
            <ul>
                <li>HTML5 & CSS3</li>
                <li>JavaScript & Vue.js</li>
                <li>Best Practices</li>
            </ul>
        `,
        
        // Sanitized user content
        sanitizedUserContent: '<p>Clean user content</p>',
        
        // Rich text editor output
        editorContent: '<p><strong>Bold text</strong> and <em>italic text</em></p>'
    }
});
</script>
```

**🛡️ Best Practices for v-html:**
```javascript
// Sanitize HTML content before using v-html
methods: {
    sanitizeHtml(html) {
        // Use DOMPurify library for production
        const div = document.createElement('div');
        div.textContent = html;
        return div.innerHTML;
    },
    
    // Or use a proper sanitization library
    safeHtml(content) {
        return DOMPurify.sanitize(content);
    }
}
```

---

## 📥 **Two-Way Data Binding - Bidirectional Sync**

### 1️⃣ **Directive v-model - Form Inputs**

**🎯 Basic Form Controls:**
```html
<div id="app">
    <form @submit.prevent="submitForm">
        <!-- Text input -->
        <div class="form-group">
            <label for="name">Nama:</label>
            <input 
                id="name"
                v-model="form.name" 
                type="text" 
                class="form-control"
                placeholder="Masukkan nama lengkap"
                required
            >
            <small class="form-text text-muted">{{ form.name.length }}/50 karakter</small>
        </div>
        
        <!-- Textarea -->
        <div class="form-group">
            <label for="description">Deskripsi:</label>
            <textarea 
                id="description"
                v-model="form.description" 
                class="form-control"
                rows="4"
                placeholder="Deskripsi singkat"
            ></textarea>
        </div>
        
        <!-- Number input -->
        <div class="form-group">
            <label for="stock">Stock:</label>
            <input 
                id="stock"
                v-model.number="form.stock" 
                type="number" 
                class="form-control"
                min="0"
                step="1"
            >
        </div>
        
        <!-- Checkbox -->
        <div class="form-group">
            <div class="form-check">
                <input 
                    id="isActive"
                    v-model="form.isActive" 
                    type="checkbox" 
                    class="form-check-input"
                >
                <label class="form-check-label" for="isActive">
                    Item Aktif
                </label>
            </div>
        </div>
        
        <!-- Radio buttons -->
        <div class="form-group">
            <label>Kategori:</label>
            <div class="form-check">
                <input 
                    id="cat-book"
                    v-model="form.category" 
                    value="book" 
                    type="radio" 
                    class="form-check-input"
                >
                <label class="form-check-label" for="cat-book">Buku</label>
            </div>
            <div class="form-check">
                <input 
                    id="cat-video"
                    v-model="form.category" 
                    value="video" 
                    type="radio" 
                    class="form-check-input"
                >
                <label class="form-check-label" for="cat-video">Video</label>
            </div>
        </div>
        
        <!-- Select dropdown -->
        <div class="form-group">
            <label for="priority">Prioritas:</label>
            <select 
                id="priority"
                v-model="form.priority" 
                class="form-control"
            >
                <option value="">Pilih prioritas</option>
                <option value="low">Rendah</option>
                <option value="medium">Sedang</option>
                <option value="high">Tinggi</option>
            </select>
        </div>
        
        <!-- Multi-select -->
        <div class="form-group">
            <label for="tags">Tags:</label>
            <select 
                id="tags"
                v-model="form.tags" 
                class="form-control"
                multiple
            >
                <option value="javascript">JavaScript</option>
                <option value="vuejs">Vue.js</option>
                <option value="html">HTML</option>
                <option value="css">CSS</option>
            </select>
            <small class="form-text text-muted">
                Selected: {{ form.tags.join(', ') }}
            </small>
        </div>
        
        <!-- Multiple checkboxes for array -->
        <div class="form-group">
            <label>Fitur:</label>
            <div class="form-check">
                <input 
                    id="feat-video"
                    v-model="form.features" 
                    value="video" 
                    type="checkbox" 
                    class="form-check-input"
                >
                <label class="form-check-label" for="feat-video">Video Tutorial</label>
            </div>
            <div class="form-check">
                <input 
                    id="feat-quiz"
                    v-model="form.features" 
                    value="quiz" 
                    type="checkbox" 
                    class="form-check-input"
                >
                <label class="form-check-label" for="feat-quiz">Quiz</label>
            </div>
            <div class="form-check">
                <input 
                    id="feat-certificate"
                    v-model="form.features" 
                    value="certificate" 
                    type="checkbox" 
                    class="form-check-input"
                >
                <label class="form-check-label" for="feat-certificate">Sertifikat</label>
            </div>
        </div>
        
        <button type="submit" class="btn btn-primary">Simpan</button>
    </form>
    
    <!-- Live preview -->
    <div class="mt-4 p-3 border">
        <h5>Live Preview:</h5>
        <pre>{{ JSON.stringify(form, null, 2) }}</pre>
    </div>
</div>

<script>
new Vue({
    el: '#app',
    data: {
        form: {
            name: '',
            description: '',
            stock: 0,
            isActive: true,
            category: '',
            priority: '',
            tags: [],
            features: []
        }
    },
    methods: {
        submitForm() {
            console.log('Form submitted:', this.form);
            alert('Form berhasil disimpan!');
        }
    }
});
</script>
```

### 2️⃣ **v-model Modifiers**

**🎯 Common Modifiers:**
```html
<div id="app">
    <!-- .lazy - Update on change event instead of input -->
    <input v-model.lazy="searchQuery" placeholder="Search (lazy)">
    <p>Search: {{ searchQuery }}</p>
    
    <!-- .number - Automatically convert to number -->
    <input v-model.number="age" type="number" placeholder="Age">
    <p>Age (number): {{ age }} ({{ typeof age }})</p>
    
    <!-- .trim - Automatically trim whitespace -->
    <input v-model.trim="username" placeholder="Username">
    <p>Username: "{{ username }}" (length: {{ username.length }})</p>
    
    <!-- Combining modifiers -->
    <input v-model.lazy.number="price" type="text" placeholder="Price">
    <p>Price: {{ price }} ({{ typeof price }})</p>
</div>

<script>
new Vue({
    el: '#app',
    data: {
        searchQuery: '',
        age: 0,
        username: '',
        price: 0
    }
});
</script>
```

### 3️⃣ **Custom v-model Implementation**

**🎯 Building Custom Components with v-model:**
```html
<div id="app">
    <!-- Custom input component -->
    <custom-input 
        v-model="message" 
        placeholder="Type something..."
    ></custom-input>
    
    <p>Message: {{ message }}</p>
    
    <!-- Custom checkbox component -->
    <custom-checkbox 
        v-model="isChecked"
        label="Accept terms and conditions"
    ></custom-checkbox>
    
    <p>Checked: {{ isChecked }}</p>
</div>

<script>
// Custom Input Component
Vue.component('custom-input', {
    props: ['value', 'placeholder'],
    template: `
        <div class="custom-input">
            <input 
                :value="value"
                @input="$emit('input', $event.target.value)"
                :placeholder="placeholder"
                class="form-control"
            >
        </div>
    `
});

// Custom Checkbox Component
Vue.component('custom-checkbox', {
    props: ['value', 'label'],
    template: `
        <div class="custom-checkbox">
            <label class="form-check-label">
                <input 
                    type="checkbox"
                    :checked="value"
                    @change="$emit('input', $event.target.checked)"
                    class="form-check-input"
                >
                {{ label }}
            </label>
        </div>
    `
});

new Vue({
    el: '#app',
    data: {
        message: '',
        isChecked: false
    }
});
</script>
```

---

## 🎯 **Attribute Binding - v-bind**

### 1️⃣ **Basic Attribute Binding**

**🎯 Common Attributes:**
```html
<div id="app">
    <!-- Image attributes -->
    <img :src="imageUrl" :alt="imageAlt" :title="imageTitle">
    
    <!-- Link attributes -->
    <a :href="linkUrl" :target="linkTarget" :title="linkTitle">
        {{ linkText }}
    </a>
    
    <!-- Class binding -->
    <div :class="dynamicClasses">
        Content with dynamic classes
    </div>
    
    <!-- Style binding -->
    <div :style="dynamicStyles">
        Content with dynamic styles
    </div>
    
    <!-- Data attributes -->
    <div :data-id="itemId" :data-category="itemCategory">
        Item information
    </div>
    
    <!-- ARIA attributes for accessibility -->
    <button 
        :aria-label="buttonLabel" 
        :aria-expanded="isExpanded"
        @click="toggle"
    >
        {{ buttonText }}
    </button>
</div>

<script>
new Vue({
    el: '#app',
    data: {
        imageUrl: 'https://picsum.photos/300/200',
        imageAlt: 'Random landscape image',
        imageTitle: 'Beautiful scenery',
        linkUrl: 'https://vuejs.org',
        linkTarget: '_blank',
        linkTitle: 'Vue.js Documentation',
        linkText: 'Learn Vue.js',
        dynamicClasses: {
            'alert': true,
            'alert-info': true,
            'fade-in': true
        },
        dynamicStyles: {
            color: '#2c3e50',
            fontSize: '18px',
            padding: '20px',
            backgroundColor: '#ecf0f1'
        },
        itemId: 123,
        itemCategory: 'books',
        buttonLabel: 'Toggle content visibility',
        isExpanded: false,
        buttonText: 'Show More'
    },
    methods: {
        toggle() {
            this.isExpanded = !this.isExpanded;
            this.buttonText = this.isExpanded ? 'Show Less' : 'Show More';
        }
    }
});
</script>
```

### 2️⃣ **Advanced Class Binding**

**🎯 Multiple Class Binding Strategies:**
```html
<div id="app">
    <!-- Object syntax -->
    <div :class="{
        'alert': true,
        'alert-success': isSuccess,
        'alert-danger': isError,
        'alert-warning': isWarning,
        'fade-in': animate,
        'large': isLarge
    }">
        Dynamic alert with object syntax
    </div>
    
    <!-- Array syntax -->
    <div :class="[
        'base-class',
        isSuccess && 'alert-success',
        isError && 'alert-danger',
        animate && 'fade-in',
        sizeClass
    ]">
        Dynamic alert with array syntax
    </div>
    
    <!-- Computed class -->
    <div :class="alertClasses">
        Dynamic alert with computed classes
    </div>
    
    <!-- Component class binding -->
    <custom-card :class="cardClasses"></custom-card>
</div>

<script>
new Vue({
    el: '#app',
    data: {
        isSuccess: true,
        isError: false,
        isWarning: false,
        animate: true,
        isLarge: false,
        sizeClass: 'medium'
    },
    computed: {
        alertClasses() {
            return {
                'alert': true,
                'alert-success': this.isSuccess,
                'alert-danger': this.isError,
                'alert-warning': this.isWarning,
                'fade-in': this.animate,
                [`size-${this.sizeClass}`]: true
            };
        },
        cardClasses() {
            return [
                'card',
                this.isSuccess ? 'border-success' : 'border-secondary',
                this.animate ? 'shadow-lg' : 'shadow'
            ];
        }
    }
});
</script>
```

### 3️⃣ **Advanced Style Binding**

**🎯 Dynamic Styling Techniques:**
```html
<div id="app">
    <!-- Object syntax for styles -->
    <div :style="{
        color: textColor,
        fontSize: fontSize + 'px',
        backgroundColor: bgColor,
        padding: padding + 'px',
        borderRadius: borderRadius + 'px',
        transform: `rotate(${rotation}deg)`,
        transition: 'all 0.3s ease'
    }">
        Dynamic styling with object syntax
    </div>
    
    <!-- Array syntax for multiple style objects -->
    <div :style="[baseStyles, themeStyles, animationStyles]">
        Dynamic styling with array syntax
    </div>
    
    <!-- Computed styles -->
    <div :style="computedStyles">
        Dynamic styling with computed styles
    </div>
    
    <!-- Responsive styles -->
    <div :style="responsiveStyles">
        Responsive dynamic styles
    </div>
</div>

<script>
new Vue({
    el: '#app',
    data: {
        textColor: '#2c3e50',
        fontSize: 16,
        bgColor: '#ecf0f1',
        padding: 20,
        borderRadius: 8,
        rotation: 0,
        baseStyles: {
            fontFamily: 'Arial, sans-serif',
            lineHeight: 1.6
        },
        themeStyles: {
            backgroundColor: '#3498db',
            color: 'white'
        },
        animationStyles: {
            transition: 'all 0.3s ease'
        },
        windowWidth: window.innerWidth
    },
    computed: {
        computedStyles() {
            return {
                color: this.textColor,
                fontSize: `${this.fontSize}px`,
                backgroundColor: this.bgColor,
                padding: `${this.padding}px`,
                borderRadius: `${this.borderRadius}px`,
                transform: `rotate(${this.rotation}deg)`,
                boxShadow: `0 ${this.padding/4}px ${this.padding/2}px rgba(0,0,0,0.1)`,
                transition: 'all 0.3s ease'
            };
        },
        responsiveStyles() {
            return {
                fontSize: this.windowWidth < 768 ? '14px' : '16px',
                padding: this.windowWidth < 768 ? '10px' : '20px'
            };
        }
    },
    mounted() {
        // Update window width on resize
        window.addEventListener('resize', () => {
            this.windowWidth = window.innerWidth;
        });
        
        // Animate rotation
        setInterval(() => {
            this.rotation = (this.rotation + 1) % 360;
        }, 50);
    }
});
</script>
```

---

## ⚡ **Performance Optimization Tips**

### 🎯 **Best Practices for Data Binding**

```html
<div id="app">
    <!-- ✅ GOOD: Use computed properties for complex expressions -->
    <p>{{ formattedPrice }}</p>
    
    <!-- ❌ AVOID: Complex logic in templates -->
    <p>{{ price * quantity * (1 + taxRate) | currency }}</p>
    
    <!-- ✅ GOOD: Use v-once for static content -->
    <h1 v-once>{{ staticTitle }}</h1>
    
    <!-- ✅ GOOD: Use key for efficient list rendering -->
    <div v-for="item in items" :key="item.id">
        {{ item.name }}
    </div>
    
    <!-- ✅ GOOD: Debounce input events -->
    <input @input="debouncedSearch">
    
    <!-- ✅ GOOD: Use lazy modifier for large forms -->
    <textarea v-model.lazy="largeText"></textarea>
</div>

<script>
new Vue({
    el: '#app',
    data: {
        price: 100,
        quantity: 2,
        taxRate: 0.1,
        staticTitle: 'SITTA Platform',
        items: [],
        searchQuery: '',
        largeText: ''
    },
    computed: {
        formattedPrice() {
            return this.formatCurrency(this.price * this.quantity * (1 + this.taxRate));
        }
    },
    methods: {
        formatCurrency(amount) {
            return new Intl.NumberFormat('id-ID', {
                style: 'currency',
                currency: 'IDR'
            }).format(amount);
        },
        
        // Debounced search
        debouncedSearch: _.debounce(function(event) {
            this.searchQuery = event.target.value;
            this.performSearch();
        }, 300),
        
        performSearch() {
            // Perform actual search
            console.log('Searching for:', this.searchQuery);
        }
    }
});
</script>
```

### 🐛 **Common Pitfalls & Solutions**

```javascript
// ❌ PITFALL 1: Direct mutation of props
// props should be treated as read-only

// ✅ SOLUTION: Use local data or emit events
props: ['initialValue'],
data() {
    return {
        localValue: this.initialValue
    };
},
methods: {
    updateValue(newValue) {
        this.localValue = newValue;
        this.$emit('update', newValue);
    }
}

// ❌ PITFALL 2: Adding properties to objects reactively
// this.newProperty = 'value'; // Not reactive

// ✅ SOLUTION: Use Vue.set or this.$set
Vue.set(this.object, 'newProperty', 'value');
// or
this.$set(this.object, 'newProperty', 'value');

// ❌ PITFALL 3: Array mutation methods that aren't reactive
// this.array[index] = newValue; // Not reactive
// this.array.length = newLength; // Not reactive

// ✅ SOLUTION: Use reactive array methods
this.$set(this.array, index, newValue);
this.array.splice(newLength);

// ❌ PITFALL 4: Overusing v-html with untrusted content
// <div v-html="userInput"></div> // XSS risk

// ✅ SOLUTION: Sanitize content first
<div v-html="sanitizedHtml"></div>

computed: {
    sanitizedHtml() {
        return DOMPurify.sanitize(this.userInput);
    }
}
```

---

## 🛠️ **Debugging Data Binding Issues**

### 🎯 **Vue DevTools for Data Binding**

```javascript
// Install Vue DevTools browser extension
// Features:
// 1. Component inspection
// 2. Reactive data monitoring
// 3. Event tracking
// 4. Performance profiling

// Debugging techniques
methods: {
    debugDataBinding() {
        // Log current state
        console.log('Current data:', this.$data);
        
        // Log specific property
        console.log('User name:', this.user.name);
        
        // Watch for changes
        this.$watch('user.name', (newVal, oldVal) => {
            console.log('Name changed:', oldVal, '->', newVal);
        });
        
        // Force reactivity check
        this.$forceUpdate();
    }
}
```

---

**🎉 Congratulations! You've mastered Vue.js Data Binding!**

**📝 Key Takeaways:**
1. **One-way binding** untuk display data
2. **Two-way binding** untuk form inputs
3. **Computed properties** untuk complex logic
4. **Performance optimization** dengan proper techniques
5. **Security considerations** dengan v-html

**🚀 Next Up:** Conditional Rendering - Dynamic UI Logic

---

## 🎭 **Materi 3: Conditional Rendering - **Dynamic UI Logic**

### 🎯 **Konsep Conditional Rendering**

**📖 Definisi:** Conditional rendering adalah teknik untuk menampilkan atau menyembunyikan elemen berdasarkan kondisi tertentu. Vue.js menyediakan beberapa directive untuk hal ini.

**🌟 Types of Conditional Rendering:**
- **🔀 v-if / v-else-if / v-else**: True conditional rendering (adds/removes from DOM)
- **👁️ v-show**: Toggle visibility (CSS display property)
- **🎯 v-if with template**: Conditional block rendering
- **🔄 Dynamic components**: Component-based conditional rendering

---

## 🔀 **v-if, v-else-if, v-else - True Conditional**

### 1️⃣ **Basic Conditional Rendering**

**🎯 Simple User Role System:**
```html
<div id="app">
    <!-- User role-based content -->
    <div v-if="user.role === 'admin'">
        <div class="card border-danger">
            <div class="card-header bg-danger text-white">
                <h5 class="mb-0">🔐 Admin Dashboard</h5>
            </div>
            <div class="card-body">
                <p>Welcome, <strong>{{ user.name }}</strong>!</p>
                <p>You have full system access.</p>
                <div class="admin-actions">
                    <button class="btn btn-primary me-2">👥 Manage Users</button>
                    <button class="btn btn-warning me-2">📊 View Reports</button>
                    <button class="btn btn-danger">⚙️ System Settings</button>
                </div>
            </div>
        </div>
    </div>
    
    <div v-else-if="user.role === 'teacher'">
        <div class="card border-success">
            <div class="card-header bg-success text-white">
                <h5 class="mb-0">👨‍🏫 Teacher Dashboard</h5>
            </div>
            <div class="card-body">
                <p>Welcome, <strong>{{ user.name }}</strong>!</p>
                <p>You have teacher privileges.</p>
                <div class="teacher-actions">
                    <button class="btn btn-primary me-2">📚 Manage Courses</button>
                    <button class="btn btn-info me-2">📝 Create Assignments</button>
                    <button class="btn btn-success">📈 View Progress</button>
                </div>
            </div>
        </div>
    </div>
    
    <div v-else-if="user.role === 'student'">
        <div class="card border-primary">
            <div class="card-header bg-primary text-white">
                <h5 class="mb-0">🎓 Student Dashboard</h5>
            </div>
            <div class="card-body">
                <p>Welcome, <strong>{{ user.name }}</strong>!</p>
                <p>You have student access.</p>
                <div class="student-actions">
                    <button class="btn btn-primary me-2">📖 My Courses</button>
                    <button class="btn btn-info me-2">📋 Assignments</button>
                    <button class="btn btn-success">🏆 My Progress</button>
                </div>
            </div>
        </div>
    </div>
    
    <div v-else>
        <div class="card border-secondary">
            <div class="card-header bg-secondary text-white">
                <h5 class="mb-0">👤 Guest Access</h5>
            </div>
            <div class="card-body">
                <p>Welcome to SITTA Platform!</p>
                <p>Please login to access full features.</p>
                <div class="guest-actions">
                    <button class="btn btn-primary me-2">🔑 Login</button>
                    <button class="btn btn-outline-primary">📝 Register</button>
                </div>
            </div>
        </div>
    </div>
    
    <!-- Role switcher for demo -->
    <div class="mt-4 p-3 bg-light rounded">
        <h6>Switch Role (Demo):</h6>
        <div class="btn-group" role="group">
            <button 
                @click="switchRole('admin')" 
                class="btn btn-outline-danger"
                :class="{ active: user.role === 'admin' }"
            >
                Admin
            </button>
            <button 
                @click="switchRole('teacher')" 
                class="btn btn-outline-success"
                :class="{ active: user.role === 'teacher' }"
            >
                Teacher
            </button>
            <button 
                @click="switchRole('student')" 
                class="btn btn-outline-primary"
                :class="{ active: user.role === 'student' }"
            >
                Student
            </button>
            <button 
                @click="switchRole('guest')" 
                class="btn btn-outline-secondary"
                :class="{ active: user.role === 'guest' }"
            >
                Guest
            </button>
        </div>
    </div>
</div>

<script>
new Vue({
    el: '#app',
    data: {
        user: {
            name: 'Ahmad Rizki',
            role: 'student',
            email: 'ahmad@ut.ac.id'
        }
    },
    methods: {
        switchRole(role) {
            this.user.role = role;
            // Update name based on role for demo
            const names = {
                admin: 'Administrator',
                teacher: 'Budi Santoso, S.Kom',
                student: 'Ahmad Rizki',
                guest: 'Guest User'
            };
            this.user.name = names[role];
        }
    }
});
</script>
```

### 2️⃣ **Complex Conditional Logic**

**🎯 Multi-Condition Product Display:**
```html
<div id="app">
    <div class="container">
        <h2>📦 Product Inventory Management</h2>
        
        <!-- Product list with conditional rendering -->
        <div v-for="product in products" :key="product.id" class="card mb-3">
            <div class="card-header d-flex justify-content-between align-items-center">
                <h5 class="mb-0">{{ product.name }}</h5>
                <div>
                    <!-- Stock status badges -->
                    <span v-if="product.stock === 0" class="badge bg-danger">
                        ❌ Out of Stock
                    </span>
                    <span v-else-if="product.stock < 5" class="badge bg-warning">
                        ⚠️ Low Stock ({{ product.stock }})
                    </span>
                    <span v-else-if="product.stock < 20" class="badge bg-info">
                        📦 Limited ({{ product.stock }})
                    </span>
                    <span v-else class="badge bg-success">
                        ✅ Available ({{ product.stock }})
                    </span>
                    
                    <!-- Category badge -->
                    <span class="badge bg-secondary ms-2">{{ product.category }}</span>
                </div>
            </div>
            
            <div class="card-body">
                <div class="row">
                    <div class="col-md-8">
                        <p><strong>Price:</strong> {{ formatCurrency(product.price) }}</p>
                        <p><strong>Description:</strong> {{ product.description }}</p>
                        
                        <!-- Conditional features based on product type -->
                        <div v-if="product.category === 'book'">
                            <p><strong>Author:</strong> {{ product.author }}</p>
                            <p><strong>Pages:</strong> {{ product.pages }}</p>
                            <p><strong>ISBN:</strong> {{ product.isbn }}</p>
                        </div>
                        
                        <div v-else-if="product.category === 'video'">
                            <p><strong>Duration:</strong> {{ product.duration }}</p>
                            <p><strong>Instructor:</strong> {{ product.instructor }}</p>
                            <p><strong>Resolution:</strong> {{ product.resolution }}</p>
                        </div>
                        
                        <div v-else-if="product.category === 'software'">
                            <p><strong>Version:</strong> {{ product.version }}</p>
                            <p><strong>License:</strong> {{ product.license }}</p>
                            <p><strong>Requirements:</strong> {{ product.requirements }}</p>
                        </div>
                        
                        <!-- Special offers -->
                        <div v-if="product.hasDiscount" class="alert alert-success mt-3">
                            <strong>🎉 Special Offer!</strong><br>
                            Save {{ product.discountPercentage }}% - 
                            Only {{ formatCurrency(product.discountedPrice) }}
                        </div>
                        
                        <!-- New product badge -->
                        <div v-if="product.isNew" class="alert alert-info mt-3">
                            <strong>✨ New Product!</strong><br>
                            Just added to our catalog
                        </div>
                    </div>
                    
                    <div class="col-md-4">
                        <!-- Conditional action buttons -->
                        <div class="d-grid gap-2">
                            <button 
                                v-if="product.stock > 0"
                                @click="addToCart(product)"
                                class="btn btn-primary"
                                :disabled="product.stock < 5"
                            >
                                🛒 Add to Cart
                                <span v-if="product.stock < 5" class="text-warning">
                                    (Only {{ product.stock }} left!)
                                </span>
                            </button>
                            
                            <button 
                                v-else
                                class="btn btn-secondary"
                                disabled
                            >
                                ❌ Out of Stock
                            </button>
                            
                            <button 
                                v-if="!product.inWishlist"
                                @click="addToWishlist(product)"
                                class="btn btn-outline-danger"
                            >
                                ❤️ Add to Wishlist
                            </button>
                            
                            <button 
                                v-else
                                @click="removeFromWishlist(product)"
                                class="btn btn-danger"
                            >
                                💔 Remove from Wishlist
                            </button>
                            
                            <!-- Admin-only actions -->
                            <div v-if="userRole === 'admin'">
                                <button 
                                    @click="editProduct(product)"
                                    class="btn btn-outline-primary"
                                >
                                    ✏️ Edit
                                </button>
                                <button 
                                    @click="deleteProduct(product)"
                                    class="btn btn-outline-danger"
                                >
                                    🗑️ Delete
                                </button>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>

<script>
new Vue({
    el: '#app',
    data: {
        userRole: 'student', // Change to 'admin' to see admin features
        products: [
            {
                id: 1,
                name: 'Vue.js Complete Guide',
                category: 'book',
                stock: 25,
                price: 450000,
                description: 'Comprehensive guide to Vue.js framework',
                author: 'Sarah Johnson',
                pages: 450,
                isbn: '978-1234567890',
                hasDiscount: true,
                discountPercentage: 20,
                discountedPrice: 360000,
                isNew: true,
                inWishlist: false
            },
            {
                id: 2,
                name: 'JavaScript Advanced Course',
                category: 'video',
                stock: 3,
                price: 750000,
                description: 'Advanced JavaScript concepts and patterns',
                duration: '12 hours',
                instructor: 'Mike Chen',
                resolution: '1080p',
                hasDiscount: false,
                isNew: false,
                inWishlist: true
            },
            {
                id: 3,
                name: 'Web Development Tools Suite',
                category: 'software',
                stock: 0,
                price: 1200000,
                description: 'Complete web development toolkit',
                version: '3.0',
                license: 'Perpetual',
                requirements: 'Windows 10+, macOS 10.14+, Ubuntu 18.04+',
                hasDiscount: false,
                isNew: false,
                inWishlist: false
            }
        ]
    },
    methods: {
        formatCurrency(amount) {
            return new Intl.NumberFormat('id-ID', {
                style: 'currency',
                currency: 'IDR'
            }).format(amount);
        },
        
        addToCart(product) {
            console.log('Adding to cart:', product.name);
            alert(`${product.name} added to cart!`);
        },
        
        addToWishlist(product) {
            product.inWishlist = true;
            console.log('Added to wishlist:', product.name);
        },
        
        removeFromWishlist(product) {
            product.inWishlist = false;
            console.log('Removed from wishlist:', product.name);
        },
        
        editProduct(product) {
            console.log('Editing product:', product.name);
        },
        
        deleteProduct(product) {
            if (confirm(`Delete ${product.name}?`)) {
                const index = this.products.findIndex(p => p.id === product.id);
                this.products.splice(index, 1);
            }
        }
    }
});
</script>
```

### 3️⃣ **Template Tag with v-if**

**🎯 Conditional Block Rendering:**
```html
<div id="app">
    <!-- Using template for multiple elements with single condition -->
    <template v-if="isLoggedIn">
        <header class="bg-primary text-white p-3 mb-4">
            <div class="container">
                <div class="d-flex justify-content-between align-items-center">
                    <h1>🎓 SITTA Platform</h1>
                    <div>
                        <span class="me-3">Welcome, {{ user.name }}!</span>
                        <button @click="logout" class="btn btn-light btn-sm">Logout</button>
                    </div>
                </div>
            </div>
        </header>
        
        <nav class="bg-light p-2 mb-4">
            <div class="container">
                <ul class="nav nav-pills">
                    <li class="nav-item">
                        <a class="nav-link active" href="#">Dashboard</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Courses</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Assignments</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Profile</a>
                    </li>
                </ul>
            </div>
        </nav>
    </template>
    
    <template v-else>
        <header class="bg-secondary text-white p-3 mb-4">
            <div class="container text-center">
                <h1>🎓 SITTA Platform</h1>
                <p>Please login to access the platform</p>
            </div>
        </header>
        
        <div class="container">
            <div class="row justify-content-center">
                <div class="col-md-6">
                    <div class="card">
                        <div class="card-header">
                            <h5>Login</h5>
                        </div>
                        <div class="card-body">
                            <form @submit.prevent="login">
                                <div class="form-group mb-3">
                                    <label>Email:</label>
                                    <input 
                                        v-model="loginForm.email" 
                                        type="email" 
                                        class="form-control"
                                        required
                                    >
                                </div>
                                <div class="form-group mb-3">
                                    <label>Password:</label>
                                    <input 
                                        v-model="loginForm.password" 
                                        type="password" 
                                        class="form-control"
                                        required
                                    >
                                </div>
                                <button type="submit" class="btn btn-primary w-100">Login</button>
                            </form>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </template>
    
    <!-- Main content -->
    <main class="container">
        <template v-if="isLoggedIn">
            <div class="row">
                <div class="col-md-8">
                    <h2>📚 Your Courses</h2>
                    <div class="list-group">
                        <div v-for="course in courses" :key="course.id" class="list-group-item">
                            <h5>{{ course.title }}</h5>
                            <p>{{ course.description }}</p>
                            <div class="d-flex justify-content-between align-items-center">
                                <span class="badge bg-primary">{{ course.progress }}% Complete</span>
                                <button class="btn btn-sm btn-outline-primary">Continue</button>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col-md-4">
                    <h3>📊 Progress Overview</h3>
                    <div class="card">
                        <div class="card-body">
                            <div v-for="stat in stats" :key="stat.label" class="mb-3">
                                <strong>{{ stat.label }}:</strong>
                                <span class="float-end">{{ stat.value }}</span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </template>
        
        <template v-else>
            <div class="text-center">
                <h2>🌟 Welcome to SITTA</h2>
                <p class="lead">Your gateway to quality education</p>
                <div class="row mt-4">
                    <div class="col-md-4">
                        <div class="card h-100">
                            <div class="card-body text-center">
                                <h3>📚</h3>
                                <h5>Rich Content</h5>
                                <p>Access comprehensive learning materials</p>
                            </div>
                        </div>
                    </div>
                    <div class="col-md-4">
                        <div class="card h-100">
                            <div class="card-body text-center">
                                <h3>🎯</h3>
                                <h5>Interactive Learning</h5>
                                <p>Engage with hands-on exercises</p>
                            </div>
                        </div>
                    </div>
                    <div class="col-md-4">
                        <div class="card h-100">
                            <div class="card-body text-center">
                                <h3>🏆</h3>
                                <h5>Track Progress</h5>
                                <p>Monitor your learning journey</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </template>
    </main>
</div>

<script>
new Vue({
    el: '#app',
    data: {
        isLoggedIn: false,
        user: {
            name: 'Ahmad Rizki',
            email: 'ahmad@ut.ac.id'
        },
        loginForm: {
            email: '',
            password: ''
        },
        courses: [
            {
                id: 1,
                title: 'Web Development Fundamentals',
                description: 'Learn HTML, CSS, and JavaScript basics',
                progress: 75
            },
            {
                id: 2,
                title: 'Vue.js Framework',
                description: 'Master modern JavaScript framework',
                progress: 45
            },
            {
                id: 3,
                title: 'Database Design',
                description: 'Design and implement efficient databases',
                progress: 30
            }
        ],
        stats: [
            { label: 'Total Courses', value: '12' },
            { label: 'Completed', value: '3' },
            { label: 'In Progress', value: '5' },
            { label: 'Certificates', value: '2' }
        ]
    },
    methods: {
        login() {
            // Simulate login
            this.isLoggedIn = true;
            this.user.name = this.loginForm.email.split('@')[0];
        },
        
        logout() {
            this.isLoggedIn = false;
            this.loginForm = { email: '', password: '' };
        }
    }
});
</script>
```

---

## 👁️ **v-show - Toggle Visibility**

### 1️⃣ **Basic v-show Usage**

**🎯 Toggle Components:**
```html
<div id="app">
    <div class="container">
        <h2>🎮 Interactive Dashboard</h2>
        
        <!-- Control panel -->
        <div class="card mb-4">
            <div class="card-header">
                <h5>🎛️ Control Panel</h5>
            </div>
            <div class="card-body">
                <div class="row">
                    <div class="col-md-6">
                        <div class="form-check form-switch mb-2">
                            <input 
                                v-model="showUserPanel" 
                                class="form-check-input" 
                                type="checkbox" 
                                id="userPanel"
                            >
                            <label class="form-check-label" for="userPanel">
                                Show User Panel
                            </label>
                        </div>
                        
                        <div class="form-check form-switch mb-2">
                            <input 
                                v-model="showStats" 
                                class="form-check-input" 
                                type="checkbox" 
                                id="stats"
                            >
                            <label class="form-check-label" for="stats">
                                Show Statistics
                            </label>
                        </div>
                        
                        <div class="form-check form-switch mb-2">
                            <input 
                                v-model="showNotifications" 
                                class="form-check-input" 
                                type="checkbox" 
                                id="notifications"
                            >
                            <label class="form-check-label" for="notifications">
                                Show Notifications
                            </label>
                        </div>
                    </div>
                    
                    <div class="col-md-6">
                        <div class="form-check form-switch mb-2">
                            <input 
                                v-model="showActivity" 
                                class="form-check-input" 
                                type="checkbox" 
                                id="activity"
                            >
                            <label class="form-check-label" for="activity">
                                Show Activity Feed
                            </label>
                        </div>
                        
                        <div class="form-check form-switch mb-2">
                            <input 
                                v-model="showQuickActions" 
                                class="form-check-input" 
                                type="checkbox" 
                                id="quickActions"
                            >
                            <label class="form-check-label" for="quickActions">
                                Show Quick Actions
                            </label>
                        </div>
                        
                        <button @click="toggleAll" class="btn btn-primary btn-sm">
                            {{ allVisible ? 'Hide All' : 'Show All' }}
                        </button>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- User Panel -->
        <div v-show="showUserPanel" class="card mb-3">
            <div class="card-header bg-info text-white">
                <h5 class="mb-0">👤 User Panel</h5>
            </div>
            <div class="card-body">
                <div class="row">
                    <div class="col-md-3">
                        <img :src="user.avatar" class="img-fluid rounded-circle" alt="User Avatar">
                    </div>
                    <div class="col-md-9">
                        <h4>{{ user.name }}</h4>
                        <p><strong>Email:</strong> {{ user.email }}</p>
                        <p><strong>Role:</strong> {{ user.role }}</p>
                        <p><strong>Status:</strong> 
                            <span class="badge" :class="user.status === 'active' ? 'bg-success' : 'bg-warning'">
                                {{ user.status }}
                            </span>
                        </p>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- Statistics -->
        <div v-show="showStats" class="card mb-3">
            <div class="card-header bg-success text-white">
                <h5 class="mb-0">📊 Statistics</h5>
            </div>
            <div class="card-body">
                <div class="row text-center">
                    <div class="col-md-3">
                        <h3 class="text-primary">{{ stats.totalCourses }}</h3>
                        <p>Total Courses</p>
                    </div>
                    <div class="col-md-3">
                        <h3 class="text-success">{{ stats.completed }}</h3>
                        <p>Completed</p>
                    </div>
                    <div class="col-md-3">
                        <h3 class="text-warning">{{ stats.inProgress }}</h3>
                        <p>In Progress</p>
                    </div>
                    <div class="col-md-3">
                        <h3 class="text-info">{{ stats.certificates }}</h3>
                        <p>Certificates</p>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- Notifications -->
        <div v-show="showNotifications" class="card mb-3">
            <div class="card-header bg-warning text-dark">
                <h5 class="mb-0">🔔 Notifications</h5>
            </div>
            <div class="card-body">
                <div v-for="notification in notifications" :key="notification.id" class="alert mb-2" :class="notification.type">
                    <strong>{{ notification.title }}</strong><br>
                    <small>{{ notification.message }}</small>
                    <div class="float-end">
                        <small>{{ notification.time }}</small>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- Activity Feed -->
        <div v-show="showActivity" class="card mb-3">
            <div class="card-header bg-secondary text-white">
                <h5 class="mb-0">📈 Activity Feed</h5>
            </div>
            <div class="card-body">
                <div v-for="activity in activities" :key="activity.id" class="border-bottom pb-2 mb-2">
                    <div class="d-flex justify-content-between">
                        <div>
                            <strong>{{ activity.user }}</strong>
                            <span class="text-muted">{{ activity.action }}</span>
                        </div>
                        <small class="text-muted">{{ activity.time }}</small>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- Quick Actions -->
        <div v-show="showQuickActions" class="card">
            <div class="card-header bg-primary text-white">
                <h5 class="mb-0">⚡ Quick Actions</h5>
            </div>
            <div class="card-body">
                <div class="row">
                    <div class="col-md-3 mb-2">
                        <button class="btn btn-outline-primary w-100">📚 New Course</button>
                    </div>
                    <div class="col-md-3 mb-2">
                        <button class="btn btn-outline-success w-100">📝 Assignment</button>
                    </div>
                    <div class="col-md-3 mb-2">
                        <button class="btn btn-outline-info w-100">📊 Report</button>
                    </div>
                    <div class="col-md-3 mb-2">
                        <button class="btn btn-outline-warning w-100">⚙️ Settings</button>
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>

<script>
new Vue({
    el: '#app',
    data: {
        showUserPanel: true,
        showStats: true,
        showNotifications: false,
        showActivity: false,
        showQuickActions: true,
        
        user: {
            name: 'Ahmad Rizki',
            email: 'ahmad@ut.ac.id',
            role: 'Student',
            status: 'active',
            avatar: 'https://picsum.photos/150/150'
        },
        
        stats: {
            totalCourses: 12,
            completed: 3,
            inProgress: 5,
            certificates: 2
        },
        
        notifications: [
            {
                id: 1,
                title: 'New Assignment',
                message: 'You have a new assignment in Vue.js course',
                type: 'alert-info',
                time: '2 hours ago'
            },
            {
                id: 2,
                title: 'Course Completed',
                message: 'Congratulations! You completed HTML Basics',
                type: 'alert-success',
                time: '1 day ago'
            },
            {
                id: 3,
                title: 'Deadline Reminder',
                message: 'JavaScript assignment due in 2 days',
                type: 'alert-warning',
                time: '3 days ago'
            }
        ],
        
        activities: [
            {
                id: 1,
                user: 'You',
                action: 'completed Vue.js Chapter 3',
                time: '10 minutes ago'
            },
            {
                id: 2,
                user: 'Sarah',
                action: 'commented on your assignment',
                time: '1 hour ago'
            },
            {
                id: 3,
                user: 'You',
                action: 'enrolled in React Course',
                time: '2 hours ago'
            }
        ]
    },
    
    computed: {
        allVisible() {
            return this.showUserPanel && this.showStats && 
                   this.showNotifications && this.showActivity && 
                   this.showQuickActions;
        }
    },
    
    methods: {
        toggleAll() {
            const newState = !this.allVisible;
            this.showUserPanel = newState;
            this.showStats = newState;
            this.showNotifications = newState;
            this.showActivity = newState;
            this.showQuickActions = newState;
        }
    }
});
</script>
```

---

## ⚡ **Performance Optimization**

### 🎯 **v-if vs v-show - When to Use Which**

```html
<div id="app">
    <div class="container">
        <h2>🚀 Performance Comparison</h2>
        
        <!-- Performance metrics -->
        <div class="card mb-4">
            <div class="card-header">
                <h5>📊 Performance Metrics</h5>
            </div>
            <div class="card-body">
                <div class="row">
                    <div class="col-md-6">
                        <h6>v-if (Conditional Rendering)</h6>
                        <ul>
                            <li>✅ Elements are added/removed from DOM</li>
                            <li>✅ Better for rarely toggled content</li>
                            <li>✅ More memory efficient when hidden</li>
                            <li>✅ Lower initial render cost when false</li>
                            <li>❌ Higher toggle cost (DOM manipulation)</li>
                        </ul>
                    </div>
                    <div class="col-md-6">
                        <h6>v-show (Visibility Toggle)</h6>
                        <ul>
                            <li>✅ Elements stay in DOM</li>
                            <li>✅ Better for frequently toggled content</li>
                            <li>✅ Faster toggle (CSS only)</li>
                            <li>✅ Preserves component state</li>
                            <li>❌ Higher initial render cost</li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- Use case examples -->
        <div class="row">
            <!-- Good for v-if -->
            <div class="col-md-6">
                <div class="card">
                    <div class="card-header bg-success text-white">
                        <h6>✅ Good for v-if</h6>
                    </div>
                    <div class="card-body">
                        <div v-if="showUserSettings">
                            <h5>User Settings</h5>
                            <p>Complex form with many inputs</p>
                            <p>Only shown when user clicks settings</p>
                            <button class="btn btn-primary">Save Settings</button>
                        </div>
                        <button @click="showUserSettings = !showUserSettings" class="btn btn-outline-success">
                            Toggle Settings (v-if)
                        </button>
                    </div>
                </div>
            </div>
            
            <!-- Good for v-show -->
            <div class="col-md-6">
                <div class="card">
                    <div class="card-header bg-info text-white">
                        <h6>✅ Good for v-show</h6>
                    </div>
                    <div class="card-body">
                        <div v-show="showTooltip">
                            <div class="alert alert-info">
                                💡 This is a helpful tooltip that appears frequently
                            </div>
                        </div>
                        <button @click="showTooltip = !showTooltip" class="btn btn-outline-info">
                            Toggle Tooltip (v-show)
                        </button>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- Performance demo -->
        <div class="card mt-4">
            <div class="card-header">
                <h6>🏃‍♂️ Performance Demo</h6>
            </div>
            <div class="card-body">
                <p>Toggle speed comparison (1000 elements):</p>
                
                <div class="row">
                    <div class="col-md-6">
                        <h6>v-if Elements</h6>
                        <button @click="toggleVifElements" class="btn btn-primary mb-2">
                            Toggle {{ vifElements.length }} elements
                        </button>
                        <div v-if="showVifElements">
                            <div v-for="n in 100" :key="'vif-' + n" class="badge bg-primary me-1 mb-1">
                                {{ n }}
                            </div>
                        </div>
                    </div>
                    
                    <div class="col-md-6">
                        <h6>v-show Elements</h6>
                        <button @click="toggleVshowElements" class="btn btn-info mb-2">
                            Toggle {{ vshowElements.length }} elements
                        </button>
                        <div v-show="showVshowElements">
                            <div v-for="n in 100" :key="'vshow-' + n" class="badge bg-info me-1 mb-1">
                                {{ n }}
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>

<script>
new Vue({
    el: '#app',
    data: {
        showUserSettings: false,
        showTooltip: false,
        showVifElements: false,
        showVshowElements: false,
        vifElements: Array(100).fill(0),
        vshowElements: Array(100).fill(0)
    },
    methods: {
        toggleVifElements() {
            const start = performance.now();
            this.showVifElements = !this.showVifElements;
            const end = performance.now();
            console.log(`v-if toggle took ${end - start} milliseconds`);
        },
        
        toggleVshowElements() {
            const start = performance.now();
            this.showVshowElements = !this.showVshowElements;
            const end = performance.now();
            console.log(`v-show toggle took ${end - start} milliseconds`);
        }
    }
});
</script>
```

---

## 🔄 **Dynamic Components**

### 🎯 **Component-based Conditional Rendering**

```html
<div id="app">
    <div class="container">
        <h2>🧩 Dynamic Components</h2>
        
        <!-- Component selector -->
        <div class="card mb-4">
            <div class="card-header">
                <h5>Select Component</h5>
            </div>
            <div class="card-body">
                <div class="btn-group" role="group">
                    <button 
                        v-for="tab in tabs" 
                        :key="tab.name"
                        @click="currentTab = tab.component"
                        class="btn"
                        :class="currentTab === tab.component ? 'btn-primary' : 'btn-outline-primary'"
                    >
                        {{ tab.name }}
                    </button>
                </div>
            </div>
        </div>
        
        <!-- Dynamic component with keep-alive -->
        <keep-alive>
            <component :is="currentTab" :user="user" @update="handleUpdate"></component>
        </keep-alive>
    </div>
</div>

<script>
// Dashboard Component
Vue.component('dashboard', {
    props: ['user'],
    template: `
        <div class="card">
            <div class="card-header bg-primary text-white">
                <h5>📊 Dashboard</h5>
            </div>
            <div class="card-body">
                <p>Welcome back, {{ user.name }}!</p>
                <div class="row text-center">
                    <div class="col-md-4">
                        <h3 class="text-primary">12</h3>
                        <p>Courses</p>
                    </div>
                    <div class="col-md-4">
                        <h3 class="text-success">8</h3>
                        <p>Completed</p>
                    </div>
                    <div class="col-md-4">
                        <h3 class="text-info">4</h3>
                        <p>In Progress</p>
                    </div>
                </div>
            </div>
        </div>
    `
});

// Profile Component
Vue.component('profile', {
    props: ['user'],
    template: `
        <div class="card">
            <div class="card-header bg-success text-white">
                <h5>👤 Profile</h5>
            </div>
            <div class="card-body">
                <div class="row">
                    <div class="col-md-4">
                        <img :src="user.avatar" class="img-fluid rounded-circle" alt="Avatar">
                    </div>
                    <div class="col-md-8">
                        <h4>{{ user.name }}</h4>
                        <p><strong>Email:</strong> {{ user.email }}</p>
                        <p><strong>Role:</strong> {{ user.role }}</p>
                        <button @click="$emit('update', 'profile')" class="btn btn-primary">
                            Update Profile
                        </button>
                    </div>
                </div>
            </div>
        </div>
    `
});

// Settings Component
Vue.component('settings', {
    props: ['user'],
    template: `
        <div class="card">
            <div class="card-header bg-warning text-dark">
                <h5>⚙️ Settings</h5>
            </div>
            <div class="card-body">
                <div class="form-group mb-3">
                    <label>Display Name</label>
                    <input v-model="localUser.name" type="text" class="form-control">
                </div>
                <div class="form-group mb-3">
                    <label>Email</label>
                    <input v-model="localUser.email" type="email" class="form-control">
                </div>
                <div class="form-check mb-3">
                    <input v-model="localUser.notifications" type="checkbox" class="form-check-input">
                    <label class="form-check-label">Enable Notifications</label>
                </div>
                <button @click="saveSettings" class="btn btn-success">Save Settings</button>
            </div>
        </div>
    `,
    data() {
        return {
            localUser: { ...this.user }
        };
    },
    methods: {
        saveSettings() {
            this.$emit('update', 'settings', this.localUser);
        }
    }
});

new Vue({
    el: '#app',
    data: {
        currentTab: 'dashboard',
        user: {
            name: 'Ahmad Rizki',
            email: 'ahmad@ut.ac.id',
            role: 'Student',
            avatar: 'https://picsum.photos/150/150',
            notifications: true
        },
        tabs: [
            { name: 'Dashboard', component: 'dashboard' },
            { name: 'Profile', component: 'profile' },
            { name: 'Settings', component: 'settings' }
        ]
    },
    methods: {
        handleUpdate(type, data) {
            console.log('Update from', type, data);
            if (type === 'settings' && data) {
                this.user = { ...this.user, ...data };
            }
        }
    }
});
</script>
```

---

**🎉 Excellent! You've mastered Conditional Rendering!**

**📝 Key Takeaways:**
1. **v-if** untuk conditional rendering yang benar-benar menghapus elemen
2. **v-show** untuk toggle visibility yang cepat
3. **template tag** untuk multiple elements dengan satu kondisi
4. **Performance considerations** berdasarkan use case
5. **Dynamic components** untuk complex conditional logic

**🚀 Next Up:** Computed Properties and Methods - Smart Data Processing

---

## 🧮 **Materi 4: Computed Properties dan Methods - **Smart Data Processing**

### 🎯 **Konsep Computed Properties vs Methods**

**📖 Definisi:** Computed properties adalah properties yang dihitung berdasarkan data lain dan di-cache secara otomatis. Methods adalah fungsi yang dieksekusi setiap kali dipanggil.

**🌟 Key Differences:**
- **🧮 Computed Properties**: Cached, dependency-based, reactive
- **🔧 Methods**: Always re-execute, no caching, function calls
- **⚡ Performance**: Computed properties lebih efficient untuk derived data
- **🔄 Reactivity**: Computed properties otomatis update saat dependencies berubah

---

## 🧮 **Computed Properties - Caching & Performance**

### 1️⃣ **Basic Computed Properties**

**🎯 Simple Data Transformation:**
```html
<div id="app">
    <div class="container">
        <h2>📊 Shopping Cart Analytics</h2>
        
        <!-- Cart items -->
        <div class="card mb-4">
            <div class="card-header">
                <h5>🛒 Cart Items</h5>
            </div>
            <div class="card-body">
                <div v-for="item in cartItems" :key="item.id" class="row mb-3 align-items-center">
                    <div class="col-md-4">
                        <strong>{{ item.name }}</strong>
                        <br><small class="text-muted">{{ item.category }}</small>
                    </div>
                    <div class="col-md-2">
                        {{ formatCurrency(item.price) }}
                    </div>
                    <div class="col-md-2">
                        <div class="input-group">
                            <button @click="updateQuantity(item.id, item.quantity - 1)" class="btn btn-outline-secondary">-</button>
                            <input v-model.number="item.quantity" type="number" class="form-control text-center" min="1">
                            <button @click="updateQuantity(item.id, item.quantity + 1)" class="btn btn-outline-secondary">+</button>
                        </div>
                    </div>
                    <div class="col-md-2">
                        <strong>{{ formatCurrency(item.subtotal) }}</strong>
                    </div>
                    <div class="col-md-2">
                        <button @click="removeItem(item.id)" class="btn btn-danger btn-sm">🗑️</button>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- Computed analytics -->
        <div class="row">
            <div class="col-md-8">
                <div class="card">
                    <div class="card-header bg-primary text-white">
                        <h5>📈 Cart Analytics (Computed Properties)</h5>
                    </div>
                    <div class="card-body">
                        <div class="row text-center">
                            <div class="col-md-3">
                                <h4 class="text-primary">{{ totalItems }}</h4>
                                <p>Total Items</p>
                            </div>
                            <div class="col-md-3">
                                <h4 class="text-success">{{ totalQuantity }}</h4>
                                <p>Total Quantity</p>
                            </div>
                            <div class="col-md-3">
                                <h4 class="text-info">{{ formatCurrency(subtotal) }}</h4>
                                <p>Subtotal</p>
                            </div>
                            <div class="col-md-3">
                                <h4 class="text-warning">{{ formatCurrency(totalWithTax) }}</h4>
                                <p>Total with Tax</p>
                            </div>
                        </div>
                        
                        <hr>
                        
                        <div class="row">
                            <div class="col-md-6">
                                <h6>🏷️ Category Breakdown</h6>
                                <div v-for="(count, category) in categoryBreakdown" :key="category" class="d-flex justify-content-between">
                                    <span>{{ category }}</span>
                                    <span class="badge bg-primary">{{ count }} items</span>
                                </div>
                            </div>
                            <div class="col-md-6">
                                <h6>💰 Price Analysis</h6>
                                <div class="d-flex justify-content-between">
                                    <span>Average Price:</span>
                                    <span>{{ formatCurrency(averagePrice) }}</span>
                                </div>
                                <div class="d-flex justify-content-between">
                                    <span>Most Expensive:</span>
                                    <span>{{ formatCurrency(mostExpensive) }}</span>
                                </div>
                                <div class="d-flex justify-content-between">
                                    <span>Cheapest:</span>
                                    <span>{{ formatCurrency(cheapest) }}</span>
                                </div>
                            </div>
                        </div>
                        
                        <hr>
                        
                        <div class="row">
                            <div class="col-md-6">
                                <h6>🎯 Cart Status</h6>
                                <div class="alert" :class="cartStatusClass">
                                    <strong>{{ cartStatus }}</strong>
                                    <br><small>{{ cartMessage }}</small>
                                </div>
                            </div>
                            <div class="col-md-6">
                                <h6>🏆 Rewards Eligibility</h6>
                                <div v-for="reward in availableRewards" :key="reward.name" class="badge bg-success me-2 mb-2">
                                    🎁 {{ reward.name }}
                                </div>
                                <p v-if="availableRewards.length === 0" class="text-muted">
                                    Add {{ nextRewardThreshold - subtotal }} more for rewards!
                                </p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="col-md-4">
                <div class="card">
                    <div class="card-header bg-success text-white">
                        <h5>💡 Performance Demo</h5>
                    </div>
                    <div class="card-body">
                        <h6>Computed vs Methods</h6>
                        <button @click="runPerformanceTest" class="btn btn-primary btn-sm mb-3">
                            Run Performance Test
                        </button>
                        
                        <div v-if="performanceResults.computedTime">
                            <div class="alert alert-info">
                                <strong>Computed Properties:</strong><br>
                                {{ performanceResults.computedTime }}ms<br>
                                <small>Executed: {{ performanceResults.computedCalls }} times</small>
                            </div>
                            <div class="alert alert-warning">
                                <strong>Methods:</strong><br>
                                {{ performanceResults.methodTime }}ms<br>
                                <small>Executed: {{ performanceResults.methodCalls }} times</small>
                            </div>
                            <div class="alert alert-success">
                                <strong>Performance Gain:</strong><br>
                                {{ performanceResults.performanceGain }}x faster
                            </div>
                        </div>
                        
                        <hr>
                        
                        <h6>Caching Demo</h6>
                        <button @click="incrementCounter" class="btn btn-outline-primary btn-sm">
                            Increment Counter: {{ counter }}
                        </button>
                        <p class="mt-2">
                            <small class="text-muted">
                                Computed property only recalculates when dependencies change
                            </small>
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>

<script>
new Vue({
    el: '#app',
    data: {
        counter: 0,
        cartItems: [
            {
                id: 1,
                name: 'Vue.js Complete Guide',
                category: 'Books',
                price: 450000,
                quantity: 2
            },
            {
                id: 2,
                name: 'JavaScript Advanced Course',
                category: 'Videos',
                price: 750000,
                quantity: 1
            },
            {
                id: 3,
                name: 'Web Development Tools',
                category: 'Software',
                price: 1200000,
                quantity: 1
            },
            {
                id: 4,
                name: 'CSS Masterclass',
                category: 'Videos',
                price: 350000,
                quantity: 3
            }
        ],
        performanceResults: {
            computedTime: null,
            methodTime: null,
            computedCalls: 0,
            methodCalls: 0,
            performanceGain: 0
        }
    },
    
    computed: {
        // 🧮 Basic computed properties
        totalItems() {
            console.log('Computing totalItems...');
            return this.cartItems.length;
        },
        
        totalQuantity() {
            console.log('Computing totalQuantity...');
            return this.cartItems.reduce((sum, item) => sum + item.quantity, 0);
        },
        
        subtotal() {
            console.log('Computing subtotal...');
            return this.cartItems.reduce((sum, item) => sum + item.subtotal, 0);
        },
        
        totalWithTax() {
            console.log('Computing totalWithTax...');
            return this.subtotal * 1.1; // 10% tax
        },
        
        // 📊 Advanced computed properties
        categoryBreakdown() {
            console.log('Computing categoryBreakdown...');
            const breakdown = {};
            this.cartItems.forEach(item => {
                breakdown[item.category] = (breakdown[item.category] || 0) + 1;
            });
            return breakdown;
        },
        
        averagePrice() {
            console.log('Computing averagePrice...');
            if (this.cartItems.length === 0) return 0;
            return this.subtotal / this.totalQuantity;
        },
        
        mostExpensive() {
            console.log('Computing mostExpensive...');
            return Math.max(...this.cartItems.map(item => item.price));
        },
        
        cheapest() {
            console.log('Computing cheapest...');
            return Math.min(...this.cartItems.map(item => item.price));
        },
        
        // 🎯 Status computed properties
        cartStatus() {
            if (this.totalItems === 0) return 'Empty';
            if (this.totalItems < 3) return 'Light';
            if (this.totalItems < 6) return 'Moderate';
            return 'Full';
        },
        
        cartStatusClass() {
            const classes = {
                'Empty': 'alert-secondary',
                'Light': 'alert-info',
                'Moderate': 'alert-warning',
                'Full': 'alert-success'
            };
            return classes[this.cartStatus] || 'alert-secondary';
        },
        
        cartMessage() {
            const messages = {
                'Empty': 'Your cart is empty. Start shopping!',
                'Light': 'Great start! Add more items for better deals.',
                'Moderate': 'Nice selection! You qualify for free shipping.',
                'Full': 'Excellent! You\'re getting maximum value.'
            };
            return messages[this.cartStatus] || '';
        },
        
        // 🏆 Rewards computed properties
        availableRewards() {
            const rewards = [];
            if (this.subtotal >= 1000000) rewards.push({ name: 'Free Shipping', threshold: 1000000 });
            if (this.subtotal >= 1500000) rewards.push({ name: '5% Discount', threshold: 1500000 });
            if (this.subtotal >= 2000000) rewards.push({ name: 'Premium Support', threshold: 2000000 });
            return rewards;
        },
        
        nextRewardThreshold() {
            if (this.availableRewards.length === 0) return 1000000;
            const highestReward = Math.max(...this.availableRewards.map(r => r.threshold));
            return highestReward + 500000;
        },
        
        // 🚀 Performance demo computed
        expensiveComputed() {
            // Simulate expensive computation
            let result = 0;
            for (let i = 0; i < 1000000; i++) {
                result += Math.random();
            }
            return result + this.counter;
        }
    },
    
    methods: {
        // 🔧 Basic methods
        formatCurrency(amount) {
            return new Intl.NumberFormat('id-ID', {
                style: 'currency',
                currency: 'IDR'
            }).format(amount);
        },
        
        updateQuantity(itemId, newQuantity) {
            if (newQuantity < 1) return;
            const item = this.cartItems.find(item => item.id === itemId);
            if (item) {
                item.quantity = newQuantity;
            }
        },
        
        removeItem(itemId) {
            const index = this.cartItems.findIndex(item => item.id === itemId);
            if (index > -1) {
                this.cartItems.splice(index, 1);
            }
        },
        
        incrementCounter() {
            this.counter++;
        },
        
        // 🏃‍♂️ Performance test methods
        runPerformanceTest() {
            const iterations = 1000;
            
            // Test computed properties
            const computedStart = performance.now();
            for (let i = 0; i < iterations; i++) {
                this.totalItems;
                this.subtotal;
                this.categoryBreakdown;
            }
            const computedEnd = performance.now();
            
            // Test methods (equivalent functionality)
            const methodStart = performance.now();
            for (let i = 0; i < iterations; i++) {
                this.calculateTotalItems();
                this.calculateSubtotal();
                this.calculateCategoryBreakdown();
            }
            const methodEnd = performance.now();
            
            this.performanceResults = {
                computedTime: (computedEnd - computedStart).toFixed(2),
                methodTime: (methodEnd - methodStart).toFixed(2),
                computedCalls: iterations * 3,
                methodCalls: iterations * 3,
                performanceGain: ((methodEnd - methodStart) / (computedEnd - computedStart)).toFixed(1)
            };
        },
        
        // 🔧 Method equivalents (for performance comparison)
        calculateTotalItems() {
            return this.cartItems.length;
        },
        
        calculateSubtotal() {
            return this.cartItems.reduce((sum, item) => sum + item.subtotal, 0);
        },
        
        calculateCategoryBreakdown() {
            const breakdown = {};
            this.cartItems.forEach(item => {
                breakdown[item.category] = (breakdown[item.category] || 0) + 1;
            });
            return breakdown;
        }
    },
    
    // 🎯 Add computed property to each item for subtotal
    created() {
        this.cartItems.forEach(item => {
            Object.defineProperty(item, 'subtotal', {
                get() {
                    return this.price * this.quantity;
                }
            });
        });
    }
});
</script>
```

### 2️⃣ **Advanced Computed Properties**

**🎯 Complex Data Processing:**
```html
<div id="advanced-app">
    <div class="container">
        <h2>🔬 Advanced Computed Properties</h2>
        
        <!-- Search and filter -->
        <div class="card mb-4">
            <div class="card-header">
                <h5>🔍 Product Search & Filter</h5>
            </div>
            <div class="card-body">
                <div class="row">
                    <div class="col-md-4">
                        <input 
                            v-model="searchQuery" 
                            type="text" 
                            class="form-control" 
                            placeholder="Search products..."
                        >
                    </div>
                    <div class="col-md-3">
                        <select v-model="selectedCategory" class="form-control">
                            <option value="">All Categories</option>
                            <option v-for="category in categories" :key="category" :value="category">
                                {{ category }}
                            </option>
                        </select>
                    </div>
                    <div class="col-md-3">
                        <select v-model="sortBy" class="form-control">
                            <option value="name">Sort by Name</option>
                            <option value="price-asc">Price: Low to High</option>
                            <option value="price-desc">Price: High to Low</option>
                            <option value="rating">Sort by Rating</option>
                        </select>
                    </div>
                    <div class="col-md-2">
                        <div class="form-check">
                            <input v-model="inStockOnly" type="checkbox" class="form-check-input" id="instock">
                            <label class="form-check-label" for="instock">In Stock Only</label>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- Results -->
        <div class="row">
            <div class="col-md-8">
                <div class="card">
                    <div class="card-header d-flex justify-content-between align-items-center">
                        <h5>📦 Products ({{ filteredProducts.length }} found)</h5>
                        <div>
                            <span class="badge bg-info">{{ searchResults.totalItems }} items</span>
                            <span class="badge bg-success">{{ searchResults.inStock }} in stock</span>
                        </div>
                    </div>
                    <div class="card-body">
                        <div v-for="product in paginatedProducts" :key="product.id" class="border-bottom pb-3 mb-3">
                            <div class="row align-items-center">
                                <div class="col-md-2">
                                    <img :src="product.image" class="img-fluid" :alt="product.name">
                                </div>
                                <div class="col-md-6">
                                    <h6>{{ product.name }}</h6>
                                    <p class="text-muted mb-1">{{ product.description }}</p>
                                    <div>
                                        <span class="badge bg-secondary">{{ product.category }}</span>
                                        <span class="badge bg-warning">⭐ {{ product.rating }}</span>
                                        <span v-if="product.stock > 0" class="badge bg-success">✓ In Stock</span>
                                        <span v-else class="badge bg-danger">✗ Out of Stock</span>
                                    </div>
                                </div>
                                <div class="col-md-2">
                                    <h5>{{ formatCurrency(product.price) }}</h5>
                                    <small v-if="product.discountPrice" class="text-muted">
                                        <s>{{ formatCurrency(product.originalPrice) }}</s>
                                    </small>
                                </div>
                                <div class="col-md-2">
                                    <button class="btn btn-primary btn-sm" :disabled="product.stock === 0">
                                        🛒 Add to Cart
                                    </button>
                                </div>
                            </div>
                        </div>
                        
                        <!-- Pagination -->
                        <nav>
                            <ul class="pagination justify-content-center">
                                <li class="page-item" :class="{ disabled: currentPage === 1 }">
                                    <a class="page-link" @click="currentPage--" href="#">Previous</a>
                                </li>
                                <li v-for="page in totalPages" :key="page" class="page-item" :class="{ active: currentPage === page }">
                                    <a class="page-link" @click="currentPage = page" href="#">{{ page }}</a>
                                </li>
                                <li class="page-item" :class="{ disabled: currentPage === totalPages }">
                                    <a class="page-link" @click="currentPage++" href="#">Next</a>
                                </li>
                            </ul>
                        </nav>
                    </div>
                </div>
            </div>
            
            <div class="col-md-4">
                <div class="card">
                    <div class="card-header bg-info text-white">
                        <h5>📊 Search Analytics</h5>
                    </div>
                    <div class="card-body">
                        <h6>🔍 Search Results</h6>
                        <div class="mb-3">
                            <strong>Query:</strong> "{{ searchQuery || 'All' }}"<br>
                            <strong>Category:</strong> {{ selectedCategory || 'All' }}<br>
                            <strong>Sort:</strong> {{ sortBy }}<br>
                            <strong>Stock Filter:</strong> {{ inStockOnly ? 'Yes' : 'No' }}
                        </div>
                        
                        <h6>📈 Statistics</h6>
                        <div class="progress mb-2">
                            <div class="progress-bar bg-success" :style="{ width: searchStats.inStockPercentage + '%' }">
                                {{ searchStats.inStockPercentage }}% In Stock
                            </div>
                        </div>
                        
                        <div class="d-flex justify-content-between mb-2">
                            <span>Average Price:</span>
                            <strong>{{ formatCurrency(searchStats.averagePrice) }}</strong>
                        </div>
                        <div class="d-flex justify-content-between mb-2">
                            <span>Price Range:</span>
                            <strong>{{ formatCurrency(searchStats.minPrice) }} - {{ formatCurrency(searchStats.maxPrice) }}</strong>
                        </div>
                        <div class="d-flex justify-content-between mb-2">
                            <span>Average Rating:</span>
                            <strong>⭐ {{ searchStats.averageRating }}</strong>
                        </div>
                        
                        <h6>🏷️ Category Distribution</h6>
                        <div v-for="(count, category) in searchStats.categoryDistribution" :key="category" class="mb-1">
                            <small>{{ category }}:</small>
                            <div class="progress" style="height: 10px;">
                                <div class="progress-bar" :style="{ width: (count / searchResults.totalItems * 100) + '%' }"></div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>

<script>
new Vue({
    el: '#advanced-app',
    data: {
        searchQuery: '',
        selectedCategory: '',
        sortBy: 'name',
        inStockOnly: false,
        currentPage: 1,
        itemsPerPage: 5,
        products: [
            {
                id: 1,
                name: 'Vue.js Complete Guide',
                category: 'Books',
                price: 450000,
                originalPrice: 500000,
                discountPrice: 450000,
                rating: 4.8,
                stock: 15,
                description: 'Comprehensive Vue.js tutorial',
                image: 'https://picsum.photos/100/100?random=1'
            },
            {
                id: 2,
                name: 'JavaScript Advanced',
                category: 'Videos',
                price: 750000,
                rating: 4.6,
                stock: 0,
                description: 'Advanced JavaScript concepts',
                image: 'https://picsum.photos/100/100?random=2'
            },
            {
                id: 3,
                name: 'CSS Masterclass',
                category: 'Videos',
                price: 350000,
                rating: 4.9,
                stock: 8,
                description: 'Master CSS with modern techniques',
                image: 'https://picsum.photos/100/100?random=3'
            },
            {
                id: 4,
                name: 'React Fundamentals',
                category: 'Books',
                price: 550000,
                rating: 4.5,
                stock: 12,
                description: 'Learn React from scratch',
                image: 'https://picsum.photos/100/100?random=4'
            },
            {
                id: 5,
                name: 'Web Development Tools',
                category: 'Software',
                price: 1200000,
                rating: 4.7,
                stock: 5,
                description: 'Complete development toolkit',
                image: 'https://picsum.photos/100/100?random=5'
            },
            {
                id: 6,
                name: 'Node.js Backend',
                category: 'Books',
                price: 650000,
                rating: 4.4,
                stock: 0,
                description: 'Backend development with Node.js',
                image: 'https://picsum.photos/100/100?random=6'
            }
        ]
    },
    
    computed: {
        // 📊 Categories list
        categories() {
            const cats = [...new Set(this.products.map(p => p.category))];
            return cats.sort();
        },
        
        // 🔍 Filtered and sorted products
        filteredProducts() {
            let result = [...this.products];
            
            // Search filter
            if (this.searchQuery) {
                const query = this.searchQuery.toLowerCase();
                result = result.filter(product => 
                    product.name.toLowerCase().includes(query) ||
                    product.description.toLowerCase().includes(query) ||
                    product.category.toLowerCase().includes(query)
                );
            }
            
            // Category filter
            if (this.selectedCategory) {
                result = result.filter(product => product.category === this.selectedCategory);
            }
            
            // Stock filter
            if (this.inStockOnly) {
                result = result.filter(product => product.stock > 0);
            }
            
            // Sorting
            result.sort((a, b) => {
                switch (this.sortBy) {
                    case 'name':
                        return a.name.localeCompare(b.name);
                    case 'price-asc':
                        return a.price - b.price;
                    case 'price-desc':
                        return b.price - a.price;
                    case 'rating':
                        return b.rating - a.rating;
                    default:
                        return 0;
                }
            });
            
            return result;
        },
        
        // 📄 Paginated products
        paginatedProducts() {
            const start = (this.currentPage - 1) * this.itemsPerPage;
            const end = start + this.itemsPerPage;
            return this.filteredProducts.slice(start, end);
        },
        
        // 📄 Pagination
        totalPages() {
            return Math.ceil(this.filteredProducts.length / this.itemsPerPage);
        },
        
        // 🔍 Search results summary
        searchResults() {
            return {
                totalItems: this.filteredProducts.length,
                inStock: this.filteredProducts.filter(p => p.stock > 0).length,
                outOfStock: this.filteredProducts.filter(p => p.stock === 0).length,
                discounted: this.filteredProducts.filter(p => p.discountPrice).length
            };
        },
        
        // 📊 Search statistics
        searchStats() {
            const items = this.filteredProducts;
            
            if (items.length === 0) {
                return {
                    inStockPercentage: 0,
                    averagePrice: 0,
                    minPrice: 0,
                    maxPrice: 0,
                    averageRating: 0,
                    categoryDistribution: {}
                };
            }
            
            const inStockCount = items.filter(p => p.stock > 0).length;
            const prices = items.map(p => p.price);
            const ratings = items.map(p => p.rating);
            
            const categoryDistribution = {};
            items.forEach(product => {
                categoryDistribution[product.category] = (categoryDistribution[product.category] || 0) + 1;
            });
            
            return {
                inStockPercentage: Math.round((inStockCount / items.length) * 100),
                averagePrice: prices.reduce((sum, price) => sum + price, 0) / prices.length,
                minPrice: Math.min(...prices),
                maxPrice: Math.max(...prices),
                averageRating: (ratings.reduce((sum, rating) => sum + rating, 0) / ratings.length).toFixed(1),
                categoryDistribution
            };
        }
    },
    
    methods: {
        formatCurrency(amount) {
            return new Intl.NumberFormat('id-ID', {
                style: 'currency',
                currency: 'IDR'
            }).format(amount);
        }
    },
    
    watch: {
        // Reset pagination when filters change
        searchQuery() {
            this.currentPage = 1;
        },
        selectedCategory() {
            this.currentPage = 1;
        },
        sortBy() {
            this.currentPage = 1;
        },
        inStockOnly() {
            this.currentPage = 1;
        }
    }
});
</script>
```

### 3️⃣ **Computed Property Patterns**

**🎯 Best Practices and Advanced Patterns:**
```html
<div id="patterns-app">
    <div class="container">
        <h2>🎯 Computed Property Patterns</h2>
        
        <!-- Pattern 1: Getters and Setters -->
        <div class="card mb-4">
            <div class="card-header bg-primary text-white">
                <h5>📝 Pattern 1: Computed Getters & Setters</h5>
            </div>
            <div class="card-body">
                <div class="row">
                    <div class="col-md-6">
                        <h6>Full Name (Computed with Setter)</h6>
                        <input 
                            v-model="fullName" 
                            type="text" 
                            class="form-control"
                            placeholder="Enter full name"
                        >
                        <small class="text-muted">
                            Try: "John Doe" or "Jane Smith"
                        </small>
                    </div>
                    <div class="col-md-6">
                        <h6>Individual Names</h6>
                        <p><strong>First Name:</strong> {{ user.firstName }}</p>
                        <p><strong>Last Name:</strong> {{ user.lastName }}</p>
                    </div>
                </div>
                
                <div class="row mt-3">
                    <div class="col-md-6">
                        <h6>Price Range (Computed with Setter)</h6>
                        <input 
                            v-model="priceRange" 
                            type="text" 
                            class="form-control"
                            placeholder="e.g., 100-500"
                        >
                    </div>
                    <div class="col-md-6">
                        <h6>Individual Prices</h6>
                        <p><strong>Min Price:</strong> {{ filters.minPrice }}</p>
                        <p><strong>Max Price:</strong> {{ filters.maxPrice }}</p>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- Pattern 2: Computed with Dependencies -->
        <div class="card mb-4">
            <div class="card-header bg-success text-white">
                <h5>🔗 Pattern 2: Computed with Dependencies</h5>
            </div>
            <div class="card-body">
                <div class="row">
                    <div class="col-md-4">
                        <h6>Base Data</h6>
                        <div class="form-group mb-2">
                            <label>Base Price:</label>
                            <input v-model.number="basePrice" type="number" class="form-control">
                        </div>
                        <div class="form-group mb-2">
                            <label>Quantity:</label>
                            <input v-model.number="quantity" type="number" class="form-control">
                        </div>
                        <div class="form-group mb-2">
                            <label>Discount %:</label>
                            <input v-model.number="discount" type="number" class="form-control">
                        </div>
                        <div class="form-group mb-2">
                            <label>Tax Rate:</label>
                            <input v-model.number="taxRate" type="number" step="0.01" class="form-control">
                        </div>
                    </div>
                    <div class="col-md-4">
                        <h6>Computed Results</h6>
                        <p><strong>Subtotal:</strong> {{ formatCurrency(subtotal) }}</p>
                        <p><strong>Discount Amount:</strong> {{ formatCurrency(discountAmount) }}</p>
                        <p><strong>After Discount:</strong> {{ formatCurrency(afterDiscount) }}</p>
                        <p><strong>Tax Amount:</strong> {{ formatCurrency(taxAmount) }}</p>
                        <p><strong>Total:</strong> {{ formatCurrency(total) }}</p>
                    </div>
                    <div class="col-md-4">
                        <h6>Dependency Chain</h6>
                        <div class="small">
                            <div class="alert alert-info">
                                <strong>subtotal</strong><br>
                                Depends on: basePrice, quantity
                            </div>
                            <div class="alert alert-warning">
                                <strong>discountAmount</strong><br>
                                Depends on: subtotal, discount
                            </div>
                            <div class="alert alert-success">
                                <strong>total</strong><br>
                                Depends on: afterDiscount, taxRate
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- Pattern 3: Memoization with Computed -->
        <div class="card mb-4">
            <div class="card-header bg-warning text-dark">
                <h5>🧠 Pattern 3: Memoization & Caching</h5>
            </div>
            <div class="card-body">
                <div class="row">
                    <div class="col-md-6">
                        <h6>Expensive Computation</h6>
                        <div class="form-group mb-2">
                            <label>Input Number:</label>
                            <input v-model.number="fibInput" type="number" class="form-control" min="0" max="40">
                        </div>
                        <button @click="runFibonacci" class="btn btn-primary mb-2">
                            Calculate Fibonacci
                        </button>
                        <p><strong>Result:</strong> {{ fibonacciResult }}</p>
                        <p><strong>Calculation Time:</strong> {{ fibTime }}ms</p>
                        <p><strong>Cache Hits:</strong> {{ cacheHits }}</p>
                    </div>
                    <div class="col-md-6">
                        <h6>Cache Status</h6>
                        <div class="small">
                            <div v-for="(value, key) in fibonacciCache" :key="key" class="alert alert-secondary">
                                <strong>Fib({{ key }}):</strong> {{ value }}
                            </div>
                        </div>
                        <button @click="clearCache" class="btn btn-outline-danger btn-sm">
                            Clear Cache
                        </button>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- Pattern 4: Computed for Validation -->
        <div class="card">
            <div class="card-header bg-info text-white">
                <h5>✅ Pattern 4: Computed for Validation</h5>
            </div>
            <div class="card-body">
                <div class="row">
                    <div class="col-md-6">
                        <h6>Registration Form</h6>
                        <div class="form-group mb-2">
                            <label>Email:</label>
                            <input v-model="form.email" type="email" class="form-control" :class="{ 'is-invalid': !validation.email.valid }">
                            <div v-if="!validation.email.valid" class="invalid-feedback">
                                {{ validation.email.message }}
                            </div>
                        </div>
                        <div class="form-group mb-2">
                            <label>Password:</label>
                            <input v-model="form.password" type="password" class="form-control" :class="{ 'is-invalid': !validation.password.valid }">
                            <div v-if="!validation.password.valid" class="invalid-feedback">
                                {{ validation.password.message }}
                            </div>
                        </div>
                        <div class="form-group mb-2">
                            <label>Confirm Password:</label>
                            <input v-model="form.confirmPassword" type="password" class="form-control" :class="{ 'is-invalid': !validation.confirmPassword.valid }">
                            <div v-if="!validation.confirmPassword.valid" class="invalid-feedback">
                                {{ validation.confirmPassword.message }}
                            </div>
                        </div>
                        <div class="form-group mb-2">
                            <label>Age:</label>
                            <input v-model.number="form.age" type="number" class="form-control" :class="{ 'is-invalid': !validation.age.valid }">
                            <div v-if="!validation.age.valid" class="invalid-feedback">
                                {{ validation.age.message }}
                            </div>
                        </div>
                    </div>
                    <div class="col-md-6">
                        <h6>Validation Status</h6>
                        <div class="alert" :class="formValid ? 'alert-success' : 'alert-warning'">
                            <strong>Form Status:</strong> {{ formValid ? '✅ Valid' : '⚠️ Invalid' }}
                        </div>
                        
                        <h6>Validation Details</h6>
                        <div v-for="(field, name) in validation" :key="name" class="mb-2">
                            <span class="badge" :class="field.valid ? 'bg-success' : 'bg-danger'">
                                {{ name }}: {{ field.valid ? 'Valid' : 'Invalid' }}
                            </span>
                        </div>
                        
                        <button @click="submitForm" class="btn btn-primary" :disabled="!formValid">
                            Submit Form
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>

<script>
new Vue({
    el: '#patterns-app',
    data: {
        // Pattern 1 data
        user: {
            firstName: 'John',
            lastName: 'Doe'
        },
        filters: {
            minPrice: 100,
            maxPrice: 500
        },
        
        // Pattern 2 data
        basePrice: 100,
        quantity: 2,
        discount: 10,
        taxRate: 0.1,
        
        // Pattern 3 data
        fibInput: 10,
        fibonacciCache: {},
        cacheHits: 0,
        fibTime: 0,
        
        // Pattern 4 data
        form: {
            email: '',
            password: '',
            confirmPassword: '',
            age: ''
        }
    },
    
    computed: {
        // Pattern 1: Computed with getters and setters
        fullName: {
            get() {
                return `${this.user.firstName} ${this.user.lastName}`;
            },
            set(newValue) {
                const parts = newValue.split(' ');
                this.user.firstName = parts[0] || '';
                this.user.lastName = parts[1] || '';
            }
        },
        
        priceRange: {
            get() {
                return `${this.filters.minPrice}-${this.filters.maxPrice}`;
            },
            set(newValue) {
                const parts = newValue.split('-');
                this.filters.minPrice = parseInt(parts[0]) || 0;
                this.filters.maxPrice = parseInt(parts[1]) || 1000;
            }
        },
        
        // Pattern 2: Computed with dependencies
        subtotal() {
            return this.basePrice * this.quantity;
        },
        
        discountAmount() {
            return this.subtotal * (this.discount / 100);
        },
        
        afterDiscount() {
            return this.subtotal - this.discountAmount;
        },
        
        taxAmount() {
            return this.afterDiscount * this.taxRate;
        },
        
        total() {
            return this.afterDiscount + this.taxAmount;
        },
        
        // Pattern 3: Memoized computation
        fibonacciResult() {
            return this.fibonacci(this.fibInput);
        },
        
        // Pattern 4: Computed for validation
        validation() {
            return {
                email: {
                    valid: this.validateEmail(this.form.email),
                    message: this.form.email ? 'Invalid email format' : 'Email is required'
                },
                password: {
                    valid: this.validatePassword(this.form.password),
                    message: this.getPasswordErrorMessage()
                },
                confirmPassword: {
                    valid: this.form.password === this.form.confirmPassword && this.form.confirmPassword !== '',
                    message: 'Passwords must match'
                },
                age: {
                    valid: this.form.age >= 18 && this.form.age <= 100,
                    message: 'Age must be between 18 and 100'
                }
            };
        },
        
        formValid() {
            return Object.values(this.validation).every(field => field.valid);
        }
    },
    
    methods: {
        formatCurrency(amount) {
            return new Intl.NumberFormat('id-ID', {
                style: 'currency',
                currency: 'IDR'
            }).format(amount);
        },
        
        // Pattern 3 methods
        fibonacci(n) {
            // Check cache first
            if (this.fibonacciCache[n] !== undefined) {
                this.cacheHits++;
                return this.fibonacciCache[n];
            }
            
            const start = performance.now();
            
            // Calculate Fibonacci (expensive for large n)
            if (n <= 1) return n;
            
            let a = 0, b = 1;
            for (let i = 2; i <= n; i++) {
                [a, b] = [b, a + b];
            }
            
            const result = b;
            const end = performance.now();
            this.fibTime = (end - start).toFixed(2);
            
            // Cache the result
            this.$set(this.fibonacciCache, n, result);
            
            return result;
        },
        
        runFibonacci() {
            // Trigger computation
            this.fibonacciResult;
        },
        
        clearCache() {
            this.fibonacciCache = {};
            this.cacheHits = 0;
        },
        
        // Pattern 4 methods
        validateEmail(email) {
            const re = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
            return re.test(email);
        },
        
        validatePassword(password) {
            return password.length >= 8 && /[A-Z]/.test(password) && /[0-9]/.test(password);
        },
        
        getPasswordErrorMessage() {
            if (this.form.password.length === 0) return 'Password is required';
            if (this.form.password.length < 8) return 'Password must be at least 8 characters';
            if (!/[A-Z]/.test(this.form.password)) return 'Password must contain uppercase letter';
            if (!/[0-9]/.test(this.form.password)) return 'Password must contain number';
            return 'Invalid password';
        },
        
        submitForm() {
            if (this.formValid) {
                alert('Form submitted successfully!');
                console.log('Form data:', this.form);
            }
        }
    }
});
</script>
```

---

## 🔧 **Methods - Functions & Actions**

### 🎯 **When to Use Methods vs Computed Properties**

```html
<div id="methods-app">
    <div class="container">
        <h2>🔧 Methods vs Computed Properties</h2>
        
        <div class="card mb-4">
            <div class="card-header">
                <h5>📊 Performance Comparison</h5>
            </div>
            <div class="card-body">
                <div class="row">
                    <div class="col-md-6">
                        <h6>Computed Property (Cached)</h6>
                        <button @click="incrementCounter" class="btn btn-primary mb-2">
                            Increment: {{ counter }}
                        </button>
                        <p><strong>Computed Result:</strong> {{ cachedCalculation }}</p>
                        <p class="text-muted">Only recalculates when dependencies change</p>
                    </div>
                    <div class="col-md-6">
                        <h6>Method (Always Executes)</h6>
                        <button @click="incrementCounter" class="btn btn-info mb-2">
                            Increment: {{ counter }}
                        </button>
                        <p><strong>Method Result:</strong> {{ methodCalculation() }}</p>
                        <p class="text-muted">Executes every time it's called</p>
                    </div>
                </div>
            </div>
        </div>
        
        <div class="card">
            <div class="card-header">
                <h5>🎯 Use Cases</h5>
            </div>
            <div class="card-body">
                <div class="row">
                    <div class="col-md-6">
                        <h6>✅ Use Computed Properties When:</h6>
                        <ul>
                            <li>Deriving data from other data</li>
                            <li>You need caching for performance</li>
                            <li>Data depends on reactive properties</li>
                            <li>You want to use it like a property in templates</li>
                        </ul>
                    </div>
                    <div class="col-md-6">
                        <h6>✅ Use Methods When:</h6>
                        <ul>
                            <li>You need to pass parameters</li>
                            <li>You want to perform actions</li>
                            <li>You need to trigger side effects</li>
                            <li>You don't need caching</li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>

<script>
new Vue({
    el: '#methods-app',
    data: {
        counter: 0
    },
    computed: {
        cachedCalculation() {
            console.log('Computed property executed');
            return this.counter * 2 + Math.random();
        }
    },
    methods: {
        methodCalculation() {
            console.log('Method executed');
            return this.counter * 2 + Math.random();
        },
        incrementCounter() {
            this.counter++;
        }
    }
});
</script>
```

---

**🎉 Excellent! You've mastered Computed Properties and Methods!**

**📝 Key Takeaways:**
1. **Computed properties** untuk derived data dengan caching
2. **Methods** untuk actions dan functions dengan parameters
3. **Getters & Setters** untuk two-way computed properties
4. **Memoization** untuk expensive computations
5. **Validation patterns** dengan computed properties
6. **Performance optimization** dengan proper caching strategies

**🚀 Next Up:** Watchers - Advanced Reactivity Patterns

```html
<div id="app">
    <input v-model="firstName" placeholder="Nama Depan">
    <input v-model="lastName" placeholder="Nama Belakang">
    
    <p>Nama Lengkap: {{ fullName }}</p>
    <p>Nama Lengkap (reversed): {{ reversedFullName }}</p>
    
    <input v-model="cart" type="number" min="0">
    <p>Subtotal: Rp {{ subtotal }}</p>
    <p>Pajak (10%): Rp {{ tax }}</p>
    <p>Total: Rp {{ total }}</p>
</div>

<script>
new Vue({
    el: '#app',
    data: {
        firstName: '',
        lastName: '',
        cart: 0,
        pricePerItem: 50000
    },
    computed: {
        fullName() {
            return `${this.firstName} ${this.lastName}`.trim();
        },
        reversedFullName() {
            return this.fullName.split('').reverse().join('');
        },
        subtotal() {
            return this.cart * this.pricePerItem;
        },
        tax() {
            return this.subtotal * 0.1;
        },
        total() {
            return this.subtotal + this.tax;
        }
    }
});
</script>
```

### ✅ **Methods**
Methods adalah fungsi yang bisa dipanggil dari template:

```html
<div id="app">
    <input v-model="message" placeholder="Ketik pesan">
    
    <p>Pesan asli: {{ message }}</p>
    <p>Pesan uppercase: {{ toUpperCase(message) }}</p>
    <p>Pesan lowercase: {{ toLowerCase(message) }}</p>
    <p>Pesan capitalize: {{ capitalize(message) }}</p>
    
    <button @click="showAlert">Tampilkan Alert</button>
    <button @click="clearMessage">Hapus Pesan</button>
    
    <p>Random number: {{ getRandomNumber() }}</p>
    <button @click="generateRandom">Generate Random</button>
</div>

<script>
new Vue({
    el: '#app',
    data: {
        message: '',
        randomNumber: 0
    },
    methods: {
        toUpperCase(str) {
            return str.toUpperCase();
        },
        toLowerCase(str) {
            return str.toLowerCase();
        },
        capitalize(str) {
            return str.charAt(0).toUpperCase() + str.slice(1).toLowerCase();
        },
        showAlert() {
            alert(`Pesan Anda: ${this.message}`);
        },
        clearMessage() {
            this.message = '';
        },
        getRandomNumber() {
            return this.randomNumber;
        },
        generateRandom() {
            this.randomNumber = Math.floor(Math.random() * 1000);
        }
    }
});
</script>
```

### 📝 **Computed vs Methods**
- **Computed**: Di-cache, hanya re-evaluated saat dependencies berubah
- **Methods**: Selalu dieksekusi setiap kali dipanggil

---

## 👁️ **Materi 5: Watchers - **Advanced Reactivity Patterns**

### 🎯 **Konsep Watchers**

**📖 Definisi:** Watchers adalah fitur Vue.js untuk mengamati perubahan data dan menjalankan fungsi saat perubahan terjadi. Watchers lebih powerful daripada computed properties untuk side effects dan async operations.

**🌟 When to Use Watchers:**
- **🔄 Async Operations**: API calls, timers, animations
- **⚡ Side Effects**: DOM manipulation, logging, analytics
- **🔍 Complex Logic**: Validasi, data transformation
- **💾 Data Persistence**: localStorage, database sync
- **📊 Performance**: Debouncing, throttling

---

## 🔍 **Basic Watchers - Simple Data Monitoring**

### 1️⃣ **Simple Property Watching**

**🎯 Search with Debouncing:**
```html
<div id="watcher-basic">
    <div class="container">
        <h2>🔍 Real-time Search with Watchers</h2>
        
        <div class="card mb-4">
            <div class="card-header">
                <h5>📚 Course Search</h5>
            </div>
            <div class="card-body">
                <div class="row">
                    <div class="col-md-8">
                        <div class="form-group">
                            <label for="searchInput">Search Courses:</label>
                            <input 
                                id="searchInput"
                                v-model="searchQuery" 
                                type="text" 
                                class="form-control"
                                placeholder="Type to search courses..."
                            >
                            <small class="text-muted">
                                {{ searchStatus }}
                            </small>
                        </div>
                    </div>
                    <div class="col-md-4">
                        <div class="form-group">
                            <label>Search Options:</label>
                            <div class="form-check">
                                <input v-model="searchOptions.caseSensitive" type="checkbox" class="form-check-input" id="caseSensitive">
                                <label class="form-check-label" for="caseSensitive">Case Sensitive</label>
                            </div>
                            <div class="form-check">
                                <input v-model="searchOptions.exactMatch" type="checkbox" class="form-check-input" id="exactMatch">
                                <label class="form-check-label" for="exactMatch">Exact Match</label>
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- Search Results -->
                <div v-if="isSearching" class="text-center my-3">
                    <div class="spinner-border text-primary" role="status">
                        <span class="visually-hidden">Searching...</span>
                    </div>
                    <p class="mt-2">Searching courses...</p>
                </div>
                
                <div v-else-if="searchResults.length > 0" class="mt-3">
                    <h6>Found {{ searchResults.length }} courses:</h6>
                    <div class="list-group">
                        <div v-for="course in searchResults" :key="course.id" class="list-group-item">
                            <div class="d-flex justify-content-between align-items-center">
                                <div>
                                    <h6 class="mb-1">{{ course.title }}</h6>
                                    <p class="mb-1">{{ course.description }}</p>
                                    <small class="text-muted">{{ course.category }} • {{ course.duration }}</small>
                                </div>
                                <div class="text-end">
                                    <strong>{{ formatCurrency(course.price) }}</strong>
                                    <br><small class="text-muted">⭐ {{ course.rating }}</small>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div v-else-if="searchQuery && !isSearching" class="alert alert-info mt-3">
                    No courses found for "{{ searchQuery }}"
                </div>
            </div>
        </div>
        
        <!-- Search History -->
        <div class="card">
            <div class="card-header">
                <h5>📜 Search History</h5>
            </div>
            <div class="card-body">
                <div v-if="searchHistory.length === 0" class="text-muted">
                    No search history yet
                </div>
                <div v-else>
                    <button 
                        v-for="(term, index) in searchHistory" 
                        :key="index"
                        @click="searchQuery = term"
                        class="btn btn-outline-primary btn-sm me-2 mb-2"
                    >
                        {{ term }}
                    </button>
                </div>
                <button v-if="searchHistory.length > 0" @click="clearHistory" class="btn btn-outline-danger btn-sm mt-2">
                    Clear History
                </button>
            </div>
        </div>
    </div>
</div>

<script>
new Vue({
    el: '#watcher-basic',
    data: {
        searchQuery: '',
        searchResults: [],
        searchHistory: [],
        isSearching: false,
        searchStatus: 'Ready to search',
        searchOptions: {
            caseSensitive: false,
            exactMatch: false
        },
        allCourses: [
            {
                id: 1,
                title: 'Vue.js Complete Guide',
                description: 'Learn Vue.js from scratch to advanced',
                category: 'Web Development',
                duration: '12 hours',
                price: 450000,
                rating: 4.8
            },
            {
                id: 2,
                title: 'JavaScript Advanced',
                description: 'Master advanced JavaScript concepts',
                category: 'Programming',
                duration: '8 hours',
                price: 350000,
                rating: 4.6
            },
            {
                id: 3,
                title: 'CSS Masterclass',
                description: 'Become a CSS expert',
                category: 'Web Design',
                duration: '6 hours',
                price: 280000,
                rating: 4.9
            },
            {
                id: 4,
                title: 'React Fundamentals',
                description: 'Learn React.js basics',
                category: 'Web Development',
                duration: '10 hours',
                price: 420000,
                rating: 4.5
            },
            {
                id: 5,
                title: 'Node.js Backend',
                description: 'Build backend with Node.js',
                category: 'Backend Development',
                duration: '15 hours',
                price: 550000,
                rating: 4.7
            }
        ],
        searchTimeout: null
    },
    
    watch: {
        // 🔍 Watch search query with debouncing
        searchQuery(newVal, oldVal) {
            console.log(`Search changed from "${oldVal}" to "${newVal}"`);
            
            // Clear existing timeout
            if (this.searchTimeout) {
                clearTimeout(this.searchTimeout);
            }
            
            if (newVal.trim() === '') {
                this.searchResults = [];
                this.searchStatus = 'Ready to search';
                return;
            }
            
            this.searchStatus = 'Typing...';
            
            // Debounce search (wait 500ms after user stops typing)
            this.searchTimeout = setTimeout(() => {
                this.performSearch(newVal);
            }, 500);
        },
        
        // 🔍 Watch search options
        'searchOptions.caseSensitive'() {
            if (this.searchQuery) {
                this.performSearch(this.searchQuery);
            }
        },
        
        'searchOptions.exactMatch'() {
            if (this.searchQuery) {
                this.performSearch(this.searchQuery);
            }
        }
    },
    
    methods: {
        performSearch(query) {
            this.isSearching = true;
            this.searchStatus = 'Searching...';
            
            // Simulate API call delay
            setTimeout(() => {
                const searchTerm = this.searchOptions.caseSensitive ? query : query.toLowerCase();
                
                this.searchResults = this.allCourses.filter(course => {
                    const title = this.searchOptions.caseSensitive ? course.title : course.title.toLowerCase();
                    const description = this.searchOptions.caseSensitive ? course.description : course.description.toLowerCase();
                    
                    if (this.searchOptions.exactMatch) {
                        return title === searchTerm || description === searchTerm;
                    } else {
                        return title.includes(searchTerm) || description.includes(searchTerm);
                    }
                });
                
                // Add to search history
                if (query && !this.searchHistory.includes(query)) {
                    this.searchHistory.unshift(query);
                    if (this.searchHistory.length > 5) {
                        this.searchHistory.pop();
                    }
                }
                
                this.isSearching = false;
                this.searchStatus = `Found ${this.searchResults.length} results`;
            }, 800);
        },
        
        formatCurrency(amount) {
            return new Intl.NumberFormat('id-ID', {
                style: 'currency',
                currency: 'IDR'
            }).format(amount);
        },
        
        clearHistory() {
            this.searchHistory = [];
        }
    },
    
    beforeDestroy() {
        // Cleanup timeout
        if (this.searchTimeout) {
            clearTimeout(this.searchTimeout);
        }
    }
});
</script>
```

---

## 🔬 **Deep Watchers - Nested Object Monitoring**

### 2️⃣ **Deep Object Watching**

**🎯 Complex Form Validation:**
```html
<div id="watcher-deep">
    <div class="container">
        <h2>🔬 Deep Watcher - Complex Form</h2>
        
        <div class="card">
            <div class="card-header">
                <h5>📝 Student Registration Form</h5>
            </div>
            <div class="card-body">
                <!-- Personal Information -->
                <div class="row mb-4">
                    <div class="col-md-12">
                        <h6>👤 Personal Information</h6>
                    </div>
                    <div class="col-md-6">
                        <div class="form-group mb-3">
                            <label for="firstName">First Name:</label>
                            <input 
                                id="firstName"
                                v-model="form.personal.firstName" 
                                type="text" 
                                class="form-control"
                                :class="{ 'is-invalid': errors.firstName }"
                            >
                            <div v-if="errors.firstName" class="invalid-feedback">
                                {{ errors.firstName }}
                            </div>
                        </div>
                    </div>
                    <div class="col-md-6">
                        <div class="form-group mb-3">
                            <label for="lastName">Last Name:</label>
                            <input 
                                id="lastName"
                                v-model="form.personal.lastName" 
                                type="text" 
                                class="form-control"
                                :class="{ 'is-invalid': errors.lastName }"
                            >
                            <div v-if="errors.lastName" class="invalid-feedback">
                                {{ errors.lastName }}
                            </div>
                        </div>
                    </div>
                    <div class="col-md-6">
                        <div class="form-group mb-3">
                            <label for="email">Email:</label>
                            <input 
                                id="email"
                                v-model="form.personal.email" 
                                type="email" 
                                class="form-control"
                                :class="{ 'is-invalid': errors.email }"
                            >
                            <div v-if="errors.email" class="invalid-feedback">
                                {{ errors.email }}
                            </div>
                        </div>
                    </div>
                    <div class="col-md-6">
                        <div class="form-group mb-3">
                            <label for="phone">Phone:</label>
                            <input 
                                id="phone"
                                v-model="form.personal.phone" 
                                type="tel" 
                                class="form-control"
                                :class="{ 'is-invalid': errors.phone }"
                            >
                            <div v-if="errors.phone" class="invalid-feedback">
                                {{ errors.phone }}
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- Academic Information -->
                <div class="row mb-4">
                    <div class="col-md-12">
                        <h6>🎓 Academic Information</h6>
                    </div>
                    <div class="col-md-6">
                        <div class="form-group mb-3">
                            <label for="studentId">Student ID:</label>
                            <input 
                                id="studentId"
                                v-model="form.academic.studentId" 
                                type="text" 
                                class="form-control"
                                :class="{ 'is-invalid': errors.studentId }"
                            >
                            <div v-if="errors.studentId" class="invalid-feedback">
                                {{ errors.studentId }}
                            </div>
                        </div>
                    </div>
                    <div class="col-md-6">
                        <div class="form-group mb-3">
                            <label for="major">Major:</label>
                            <select 
                                id="major"
                                v-model="form.academic.major" 
                                class="form-control"
                                :class="{ 'is-invalid': errors.major }"
                            >
                                <option value="">Select Major</option>
                                <option value="cs">Computer Science</option>
                                <option value="it">Information Technology</option>
                                <option value="is">Information Systems</option>
                                <option value="se">Software Engineering</option>
                            </select>
                            <div v-if="errors.major" class="invalid-feedback">
                                {{ errors.major }}
                            </div>
                        </div>
                    </div>
                    <div class="col-md-6">
                        <div class="form-group mb-3">
                            <label for="semester">Semester:</label>
                            <input 
                                id="semester"
                                v-model.number="form.academic.semester" 
                                type="number" 
                                min="1" 
                                max="8"
                                class="form-control"
                                :class="{ 'is-invalid': errors.semester }"
                            >
                            <div v-if="errors.semester" class="invalid-feedback">
                                {{ errors.semester }}
                            </div>
                        </div>
                    </div>
                    <div class="col-md-6">
                        <div class="form-group mb-3">
                            <label for="gpa">GPA:</label>
                            <input 
                                id="gpa"
                                v-model.number="form.academic.gpa" 
                                type="number" 
                                min="0" 
                                max="4" 
                                step="0.01"
                                class="form-control"
                                :class="{ 'is-invalid': errors.gpa }"
                            >
                            <div v-if="errors.gpa" class="invalid-feedback">
                                {{ errors.gpa }}
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- Course Selection -->
                <div class="row mb-4">
                    <div class="col-md-12">
                        <h6>📚 Course Selection</h6>
                    </div>
                    <div class="col-md-12">
                        <div v-for="(course, index) in form.courses" :key="index" class="border p-3 mb-3">
                            <div class="row">
                                <div class="col-md-4">
                                    <div class="form-group">
                                        <label>Course Code:</label>
                                        <input 
                                            v-model="course.code" 
                                            type="text" 
                                            class="form-control"
                                            placeholder="e.g., CS101"
                                        >
                                    </div>
                                </div>
                                <div class="col-md-4">
                                    <div class="form-group">
                                        <label>Course Name:</label>
                                        <input 
                                            v-model="course.name" 
                                            type="text" 
                                            class="form-control"
                                            placeholder="e.g., Introduction to Programming"
                                        >
                                    </div>
                                </div>
                                <div class="col-md-3">
                                    <div class="form-group">
                                        <label>Credits:</label>
                                        <input 
                                            v-model.number="course.credits" 
                                            type="number" 
                                            min="1" 
                                            max="6"
                                            class="form-control"
                                        >
                                    </div>
                                </div>
                                <div class="col-md-1">
                                    <div class="form-group">
                                        <label>&nbsp;</label><br>
                                        <button @click="removeCourse(index)" class="btn btn-danger btn-sm">
                                            🗑️
                                        </button>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <button @click="addCourse" class="btn btn-outline-primary">
                            ➕ Add Course
                        </button>
                    </div>
                </div>
                
                <!-- Form Status -->
                <div class="row">
                    <div class="col-md-6">
                        <div class="alert" :class="formStatusClass">
                            <strong>Form Status:</strong> {{ formStatus }}
                        </div>
                    </div>
                    <div class="col-md-6">
                        <div class="text-end">
                            <button @click="resetForm" class="btn btn-outline-secondary me-2">
                                🔄 Reset Form
                            </button>
                            <button @click="submitForm" class="btn btn-primary" :disabled="!isFormValid">
                                ✅ Submit Form
                            </button>
                        </div>
                    </div>
                </div>
                
                <!-- Form Data Preview -->
                <div class="mt-4">
                    <h6>📋 Form Data Preview:</h6>
                    <pre class="bg-light p-3 rounded">{{ JSON.stringify(form, null, 2) }}</pre>
                </div>
            </div>
        </div>
    </div>
</div>

<script>
new Vue({
    el: '#watcher-deep',
    data: {
        form: {
            personal: {
                firstName: '',
                lastName: '',
                email: '',
                phone: ''
            },
            academic: {
                studentId: '',
                major: '',
                semester: 1,
                gpa: 0
            },
            courses: [
                { code: '', name: '', credits: 3 }
            ]
        },
        errors: {},
        formStatus: 'Incomplete',
        lastSaved: null
    },
    
    computed: {
        isFormValid() {
            return this.formStatus === 'Valid';
        },
        
        formStatusClass() {
            const classes = {
                'Incomplete': 'alert-warning',
                'Valid': 'alert-success',
                'Error': 'alert-danger'
            };
            return classes[this.formStatus] || 'alert-secondary';
        },
        
        totalCredits() {
            return this.form.courses.reduce((sum, course) => sum + (course.credits || 0), 0);
        }
    },
    
    watch: {
        // 🔬 Deep watch entire form object
        form: {
            handler(newForm, oldForm) {
                console.log('Form changed:', newForm);
                
                // Validate form
                this.validateForm();
                
                // Auto-save to localStorage
                this.autoSave();
                
                // Update form status
                this.updateFormStatus();
            },
            deep: true, // Watch nested properties
            immediate: true // Run immediately on component creation
        },
        
        // 🔬 Watch specific nested properties
        'form.academic.gpa'(newGpa) {
            if (newGpa > 4.0) {
                this.$set(this.form.academic, 'gpa', 4.0);
                this.showNotification('GPA cannot exceed 4.0', 'warning');
            } else if (newGpa < 0) {
                this.$set(this.form.academic, 'gpa', 0);
                this.showNotification('GPA cannot be negative', 'warning');
            }
        },
        
        'form.academic.semester'(newSemester) {
            if (newSemester > 8) {
                this.$set(this.form.academic, 'semester', 8);
                this.showNotification('Semester cannot exceed 8', 'warning');
            } else if (newSemester < 1) {
                this.$set(this.form.academic, 'semester', 1);
                this.showNotification('Semester cannot be less than 1', 'warning');
            }
        },
        
        // 🔬 Watch courses array
        'form.courses': {
            handler(newCourses) {
                if (this.totalCredits > 24) {
                    this.showNotification('Total credits cannot exceed 24', 'warning');
                }
            },
            deep: true
        }
    },
    
    methods: {
        validateForm() {
            this.errors = {};
            
            // Validate personal information
            if (!this.form.personal.firstName.trim()) {
                this.errors.firstName = 'First name is required';
            }
            
            if (!this.form.personal.lastName.trim()) {
                this.errors.lastName = 'Last name is required';
            }
            
            if (!this.form.personal.email.trim()) {
                this.errors.email = 'Email is required';
            } else if (!this.isValidEmail(this.form.personal.email)) {
                this.errors.email = 'Invalid email format';
            }
            
            if (!this.form.personal.phone.trim()) {
                this.errors.phone = 'Phone is required';
            }
            
            // Validate academic information
            if (!this.form.academic.studentId.trim()) {
                this.errors.studentId = 'Student ID is required';
            }
            
            if (!this.form.academic.major) {
                this.errors.major = 'Major is required';
            }
            
            if (this.form.academic.semester < 1 || this.form.academic.semester > 8) {
                this.errors.semester = 'Semester must be between 1 and 8';
            }
            
            if (this.form.academic.gpa < 0 || this.form.academic.gpa > 4) {
                this.errors.gpa = 'GPA must be between 0 and 4';
            }
        },
        
        updateFormStatus() {
            const hasErrors = Object.keys(this.errors).length > 0;
            const hasPersonalData = Object.values(this.form.personal).some(val => val.toString().trim());
            const hasAcademicData = Object.values(this.form.academic).some(val => val.toString().trim());
            
            if (hasErrors) {
                this.formStatus = 'Error';
            } else if (hasPersonalData && hasAcademicData) {
                this.formStatus = 'Valid';
            } else {
                this.formStatus = 'Incomplete';
            }
        },
        
        autoSave() {
            // Save to localStorage with timestamp
            const formData = {
                ...this.form,
                timestamp: new Date().toISOString()
            };
            localStorage.setItem('studentForm', JSON.stringify(formData));
            this.lastSaved = new Date();
        },
        
        addCourse() {
            this.form.courses.push({ code: '', name: '', credits: 3 });
        },
        
        removeCourse(index) {
            if (this.form.courses.length > 1) {
                this.form.courses.splice(index, 1);
            }
        },
        
        resetForm() {
            this.form = {
                personal: {
                    firstName: '',
                    lastName: '',
                    email: '',
                    phone: ''
                },
                academic: {
                    studentId: '',
                    major: '',
                    semester: 1,
                    gpa: 0
                },
                courses: [{ code: '', name: '', credits: 3 }]
            };
            localStorage.removeItem('studentForm');
            this.showNotification('Form reset successfully', 'success');
        },
        
        submitForm() {
            if (this.isFormValid) {
                console.log('Form submitted:', this.form);
                this.showNotification('Form submitted successfully!', 'success');
                // Here you would normally send data to server
            }
        },
        
        isValidEmail(email) {
            const re = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
            return re.test(email);
        },
        
        showNotification(message, type) {
            // Simple notification (in real app, use a notification component)
            console.log(`[${type.toUpperCase()}] ${message}`);
        }
    },
    
    mounted() {
        // Load saved form data if exists
        const savedForm = localStorage.getItem('studentForm');
        if (savedForm) {
            try {
                const parsed = JSON.parse(savedForm);
                this.form = { ...parsed };
                delete this.form.timestamp; // Remove timestamp from form data
                this.showNotification('Form data restored from localStorage', 'info');
            } catch (e) {
                console.error('Error loading saved form:', e);
            }
        }
    }
});
</script>
```

---

## ⚡ **Advanced Watcher Patterns**

### 3️⃣ **Immediate & Async Watchers**

**🎯 Real-time Data Synchronization:**
```html
<div id="watcher-advanced">
    <div class="container">
        <h2>⚡ Advanced Watcher Patterns</h2>
        
        <div class="row">
            <div class="col-md-6">
                <div class="card mb-4">
                    <div class="card-header bg-primary text-white">
                        <h5>🔄 Real-time Sync</h5>
                    </div>
                    <div class="card-body">
                        <div class="form-group mb-3">
                            <label>User Profile:</label>
                            <input 
                                v-model="profile.name" 
                                type="text" 
                                class="form-control mb-2"
                                placeholder="Name"
                            >
                            <input 
                                v-model="profile.email" 
                                type="email" 
                                class="form-control mb-2"
                                placeholder="Email"
                            >
                            <textarea 
                                v-model="profile.bio" 
                                class="form-control"
                                placeholder="Bio"
                                rows="3"
                            ></textarea>
                        </div>
                        
                        <div class="form-group">
                            <label>Preferences:</label>
                            <div class="form-check">
                                <input v-model="preferences.notifications" type="checkbox" class="form-check-input" id="notifications">
                                <label class="form-check-label" for="notifications">Enable Notifications</label>
                            </div>
                            <div class="form-check">
                                <input v-model="preferences.darkMode" type="checkbox" class="form-check-input" id="darkMode">
                                <label class="form-check-label" for="darkMode">Dark Mode</label>
                            </div>
                        </div>
                        
                        <div class="mt-3">
                            <small class="text-muted">
                                Last sync: {{ lastSync ? lastSync.toLocaleTimeString() : 'Never' }}
                            </small>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="col-md-6">
                <div class="card mb-4">
                    <div class="card-header bg-success text-white">
                        <h5>📊 Sync Status</h5>
                    </div>
                    <div class="card-body">
                        <div class="mb-3">
                            <strong>Sync Status:</strong>
                            <span class="badge ms-2" :class="syncStatusClass">
                                {{ syncStatus }}
                            </span>
                        </div>
                        
                        <div class="mb-3">
                            <strong>Queue Length:</strong> {{ syncQueue.length }}
                        </div>
                        
                        <div class="mb-3">
                            <strong>Failed Attempts:</strong> {{ failedAttempts }}
                        </div>
                        
                        <div class="mb-3">
                            <strong>Auto-sync:</strong>
                            <span class="badge" :class="autoSync ? 'bg-success' : 'bg-secondary'">
                                {{ autoSync ? 'Enabled' : 'Disabled' }}
                            </span>
                        </div>
                        
                        <div class="form-check mb-3">
                            <input v-model="autoSync" type="checkbox" class="form-check-input" id="autoSync">
                            <label class="form-check-label" for="autoSync">Enable Auto-sync</label>
                        </div>
                        
                        <button @click="manualSync" class="btn btn-primary btn-sm">
                            🔄 Manual Sync
                        </button>
                        <button @click="clearQueue" class="btn btn-outline-danger btn-sm ms-2">
                            🗑️ Clear Queue
                        </button>
                    </div>
                </div>
                
                <div class="card">
                    <div class="card-header bg-info text-white">
                        <h5>📝 Sync Log</h5>
                    </div>
                    <div class="card-body">
                        <div v-if="syncLog.length === 0" class="text-muted">
                            No sync activities yet
                        </div>
                        <div v-else style="max-height: 200px; overflow-y: auto;">
                            <div v-for="(log, index) in syncLog" :key="index" class="border-bottom pb-2 mb-2">
                                <small class="text-muted">{{ log.timestamp.toLocaleTimeString() }}</small>
                                <div :class="log.type === 'error' ? 'text-danger' : log.type === 'success' ? 'text-success' : 'text-info'">
                                    {{ log.message }}
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        
        <div class="card">
            <div class="card-header bg-warning text-dark">
                <h5>🎯 API Rate Limiting</h5>
            </div>
            <div class="card-body">
                <div class="row">
                    <div class="col-md-6">
                        <div class="form-group">
                            <label>Search Query:</label>
                            <input 
                                v-model="apiQuery" 
                                type="text" 
                                class="form-control"
                                placeholder="Type to search (rate limited)"
                            >
                            <small class="text-muted">
                                API calls: {{ apiCallCount }}/10 per minute
                            </small>
                        </div>
                    </div>
                    <div class="col-md-6">
                        <div class="form-group">
                            <label>Rate Limit Status:</label>
                            <div class="progress">
                                <div 
                                    class="progress-bar" 
                                    :class="rateLimitClass"
                                    :style="{ width: (apiCallCount / 10 * 100) + '%' }"
                                >
                                    {{ apiCallCount }}/10
                                </div>
                            </div>
                            <small class="text-muted">
                                Resets in: {{ rateLimitReset }}s
                            </small>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>

<script>
new Vue({
    el: '#watcher-advanced',
    data: {
        profile: {
            name: '',
            email: '',
            bio: ''
        },
        preferences: {
            notifications: false,
            darkMode: false
        },
        syncStatus: 'Idle',
        syncQueue: [],
        failedAttempts: 0,
        lastSync: null,
        autoSync: true,
        syncLog: [],
        syncTimeout: null,
        
        // API rate limiting
        apiQuery: '',
        apiCallCount: 0,
        rateLimitReset: 60,
        rateLimitTimeout: null
    },
    
    computed: {
        syncStatusClass() {
            const classes = {
                'Idle': 'bg-secondary',
                'Syncing': 'bg-primary',
                'Success': 'bg-success',
                'Error': 'bg-danger'
            };
            return classes[this.syncStatus] || 'bg-secondary';
        },
        
        rateLimitClass() {
            if (this.apiCallCount >= 8) return 'bg-danger';
            if (this.apiCallCount >= 5) return 'bg-warning';
            return 'bg-success';
        }
    },
    
    watch: {
        // ⚡ Immediate watcher - runs immediately on component creation
        'profile.name': {
            handler(newName) {
                console.log('Name changed:', newName);
                this.addToSyncQueue('profile.name', newName);
            },
            immediate: true // Run immediately with initial value
        },
        
        // ⚡ Deep watcher for entire profile
        profile: {
            handler(newProfile) {
                if (this.autoSync) {
                    this.scheduleSync();
                }
            },
            deep: true
        },
        
        // ⚡ Watcher for preferences
        preferences: {
            handler(newPrefs) {
                console.log('Preferences changed:', newPrefs);
                this.addToSyncQueue('preferences', newPrefs);
                
                // Apply dark mode immediately
                if (newPrefs.darkMode) {
                    document.body.classList.add('dark-mode');
                } else {
                    document.body.classList.remove('dark-mode');
                }
            },
            deep: true
        },
        
        // ⚡ Watcher for auto-sync toggle
        autoSync(newVal) {
            if (newVal) {
                this.scheduleSync();
            } else {
                this.cancelScheduledSync();
            }
        },
        
        // ⚡ API rate limiting watcher
        apiQuery: {
            handler(newQuery) {
                if (newQuery.trim() && this.apiCallCount < 10) {
                    this.makeApiCall(newQuery);
                } else if (this.apiCallCount >= 10) {
                    this.addSyncLog('Rate limit exceeded', 'error');
                }
            },
            debounce: 300 // Custom debounce (requires Vue 3 or custom implementation)
        }
    },
    
    methods: {
        addToSyncQueue(key, value) {
            this.syncQueue.push({
                key,
                value,
                timestamp: new Date()
            });
            
            this.addSyncLog(`Queued: ${key}`, 'info');
        },
        
        scheduleSync() {
            // Cancel existing sync
            if (this.syncTimeout) {
                clearTimeout(this.syncTimeout);
            }
            
            // Schedule new sync after 2 seconds
            this.syncTimeout = setTimeout(() => {
                this.performSync();
            }, 2000);
        },
        
        cancelScheduledSync() {
            if (this.syncTimeout) {
                clearTimeout(this.syncTimeout);
                this.syncTimeout = null;
            }
        },
        
        async performSync() {
            if (this.syncQueue.length === 0) return;
            
            this.syncStatus = 'Syncing';
            
            try {
                // Simulate API call
                await this.simulateApiCall();
                
                // Process queue
                const itemsToSync = [...this.syncQueue];
                this.syncQueue = [];
                
                // Simulate successful sync
                this.lastSync = new Date();
                this.failedAttempts = 0;
                this.syncStatus = 'Success';
                
                this.addSyncLog(`Synced ${itemsToSync.length} items`, 'success');
                
            } catch (error) {
                this.failedAttempts++;
                this.syncStatus = 'Error';
                this.addSyncLog(`Sync failed: ${error.message}`, 'error');
                
                // Retry after 5 seconds if failed attempts < 3
                if (this.failedAttempts < 3) {
                    setTimeout(() => {
                        this.performSync();
                    }, 5000);
                }
            }
        },
        
        manualSync() {
            this.performSync();
        },
        
        clearQueue() {
            this.syncQueue = [];
            this.addSyncLog('Queue cleared', 'info');
        },
        
        addSyncLog(message, type = 'info') {
            this.syncLog.unshift({
                message,
                type,
                timestamp: new Date()
            });
            
            // Keep only last 50 logs
            if (this.syncLog.length > 50) {
                this.syncLog = this.syncLog.slice(0, 50);
            }
        },
        
        async makeApiCall(query) {
            this.apiCallCount++;
            
            // Start rate limit reset timer if not already running
            if (!this.rateLimitTimeout) {
                this.startRateLimitTimer();
            }
            
            // Simulate API call
            await this.simulateApiCall();
            this.addSyncLog(`API call for: ${query}`, 'success');
        },
        
        startRateLimitTimer() {
            this.rateLimitReset = 60;
            
            this.rateLimitTimeout = setInterval(() => {
                this.rateLimitReset--;
                
                if (this.rateLimitReset <= 0) {
                    this.apiCallCount = 0;
                    this.rateLimitReset = 60;
                    this.addSyncLog('Rate limit reset', 'info');
                }
            }, 1000);
        },
        
        simulateApiCall() {
            return new Promise((resolve, reject) => {
                setTimeout(() => {
                    // Simulate 90% success rate
                    if (Math.random() > 0.1) {
                        resolve();
                    } else {
                        reject(new Error('Simulated API failure'));
                    }
                }, 500 + Math.random() * 1000);
            });
        }
    },
    
    beforeDestroy() {
        // Cleanup timeouts
        if (this.syncTimeout) {
            clearTimeout(this.syncTimeout);
        }
        if (this.rateLimitTimeout) {
            clearInterval(this.rateLimitTimeout);
        }
    }
});
</script>
```

---

**🎉 Excellent! You've mastered Advanced Watchers!**

**📝 Key Takeaways:**
1. **Basic watchers** untuk simple data monitoring
2. **Deep watchers** untuk nested object changes
3. **Immediate watchers** untuk initial execution
4. **Async operations** dengan proper error handling
5. **Debouncing & throttling** untuk performance
6. **Rate limiting** untuk API calls

**🚀 Next Up:** SITTA Stock Application - Complete Case Study

---

## 🛠️ **Studi Kasus: Aplikasi Stok Bahan Ajar SITTA - **Complete Implementation**

### 🎯 **Project Overview**

**📖 Deskripsi:** Membangun aplikasi manajemen stok bahan ajar untuk Universitas Terbuka menggunakan Vue.js dengan fitur lengkap: CRUD operations, search, filter, pagination, dan real-time updates.

**🌟 Learning Objectives:**
- **Vue.js Fundamentals**: Components, data binding, computed properties
- **State Management**: Centralized data management
- **API Integration**: Mock API calls dengan async/await
- **User Experience**: Loading states, error handling, notifications
- **Performance**: Pagination, debouncing, optimization
- **Best Practices**: Code organization, accessibility, responsive design

---

## 📂 **Project Structure**

```
sitta-stock-app/
├── 📄 index.html                 ← Landing page dengan Vue.js
├── 📄 stok.html                  ← Main stock management page
├── 📁 css/
│   ├── 📄 bootstrap.min.css      ← Bootstrap framework
│   ├── 📄 fontawesome.min.css    ← Icons
│   └── 📄 custom.css            ← Custom styling
├── 📁 js/
│   ├── 📄 vue.js                ← Vue.js framework
│   ├── 📄 data.js               ← Mock data & API simulation
│   ├── 📄 components.js         ← Reusable Vue components
│   ├── 📄 utils.js              ← Helper functions
│   └── 📄 app.js               ← Main Vue application
└── 📁 assets/
    ├── 📁 images/               ← Product images
    └── 📁 icons/                ← Custom icons
```

---

## 🎨 **Complete Implementation - stok.html**

### 📄 **HTML Structure with Vue.js Integration**

```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SITTA - Manajemen Stok Bahan Ajar | Universitas Terbuka</title>
    
    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <!-- Font Awesome -->
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" rel="stylesheet">
    <!-- Custom CSS -->
    <style>
        :root {
            --primary-color: #2c3e50;
            --secondary-color: #3498db;
            --success-color: #27ae60;
            --warning-color: #f39c12;
            --danger-color: #e74c3c;
            --light-bg: #ecf0f1;
            --dark-text: #2c3e50;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: var(--light-bg);
            color: var(--dark-text);
        }
        
        .navbar-brand {
            font-weight: bold;
            font-size: 1.5rem;
        }
        
        .card {
            border: none;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            transition: transform 0.2s;
        }
        
        .card:hover {
            transform: translateY(-2px);
        }
        
        .stock-badge {
            font-size: 0.8rem;
            padding: 0.25rem 0.5rem;
        }
        
        .stock-high { background-color: var(--success-color); }
        .stock-medium { background-color: var(--warning-color); }
        .stock-low { background-color: var(--danger-color); }
        
        .search-container {
            position: relative;
        }
        
        .search-spinner {
            position: absolute;
            right: 10px;
            top: 50%;
            transform: translateY(-50%);
        }
        
        .fade-enter-active, .fade-leave-active {
            transition: opacity 0.3s;
        }
        
        .fade-enter, .fade-leave-to {
            opacity: 0;
        }
        
        .slide-enter-active, .slide-leave-active {
            transition: all 0.3s;
        }
        
        .slide-enter, .slide-leave-to {
            transform: translateX(30px);
            opacity: 0;
        }
        
        .notification {
            position: fixed;
            top: 20px;
            right: 20px;
            z-index: 9999;
            min-width: 300px;
        }
        
        .stats-card {
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            color: white;
            border-radius: 15px;
            padding: 1.5rem;
            margin-bottom: 1rem;
        }
        
        .loading-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(255,255,255,0.8);
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 9998;
        }
        
        @media (max-width: 768px) {
            .stats-card {
                margin-bottom: 0.5rem;
            }
        }
    </style>
</head>
<body>
    <div id="app">
        <!-- Navigation -->
        <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
            <div class="container">
                <a class="navbar-brand" href="#">
                    <i class="fas fa-book-open me-2"></i>SITTA
                </a>
                <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
                    <span class="navbar-toggler-icon"></span>
                </button>
                <div class="collapse navbar-collapse" id="navbarNav">
                    <ul class="navbar-nav me-auto">
                        <li class="nav-item">
                            <a class="nav-link" href="index.html">
                                <i class="fas fa-home me-1"></i>Beranda
                            </a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link active" href="stok.html">
                                <i class="fas fa-warehouse me-1"></i>Stok
                            </a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link" href="tracking.html">
                                <i class="fas fa-truck me-1"></i>Tracking
                            </a>
                        </li>
                    </ul>
                    <ul class="navbar-nav">
                        <li class="nav-item dropdown">
                            <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown">
                                <i class="fas fa-user me-1"></i>{{ currentUser.name }}
                            </a>
                            <ul class="dropdown-menu">
                                <li><a class="dropdown-item" href="#"><i class="fas fa-cog me-2"></i>Pengaturan</a></li>
                                <li><hr class="dropdown-divider"></li>
                                <li><a class="dropdown-item" href="#"><i class="fas fa-sign-out-alt me-2"></i>Keluar</a></li>
                            </ul>
                        </li>
                    </ul>
                </div>
            </div>
        </nav>

        <!-- Main Content -->
        <main class="container-fluid py-4">
            <!-- Page Header -->
            <div class="row mb-4">
                <div class="col-12">
                    <div class="d-flex justify-content-between align-items-center">
                        <div>
                            <h1 class="h3 mb-1">
                                <i class="fas fa-warehouse me-2"></i>Manajemen Stok Bahan Ajar
                            </h1>
                            <p class="text-muted mb-0">Kelola inventaris bahan ajar Universitas Terbuka</p>
                        </div>
                        <div>
                            <button class="btn btn-outline-secondary me-2" @click="exportData">
                                <i class="fas fa-download me-1"></i>Export
                            </button>
                            <button class="btn btn-primary" @click="showAddModal = true">
                                <i class="fas fa-plus me-1"></i>Tambah Bahan Ajar
                            </button>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Statistics Cards -->
            <div class="row mb-4">
                <div class="col-md-3 col-sm-6">
                    <div class="stats-card">
                        <div class="d-flex justify-content-between align-items-center">
                            <div>
                                <h3 class="mb-0">{{ statistics.totalItems }}</h3>
                                <p class="mb-0">Total Items</p>
                            </div>
                            <div class="fs-1 opacity-50">
                                <i class="fas fa-box"></i>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col-md-3 col-sm-6">
                    <div class="stats-card">
                        <div class="d-flex justify-content-between align-items-center">
                            <div>
                                <h3 class="mb-0">{{ statistics.totalStock }}</h3>
                                <p class="mb-0">Total Stok</p>
                            </div>
                            <div class="fs-1 opacity-50">
                                <i class="fas fa-layer-group"></i>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col-md-3 col-sm-6">
                    <div class="stats-card">
                        <div class="d-flex justify-content-between align-items-center">
                            <div>
                                <h3 class="mb-0">{{ statistics.lowStockItems }}</h3>
                                <p class="mb-0">Stok Rendah</p>
                            </div>
                            <div class="fs-1 opacity-50">
                                <i class="fas fa-exclamation-triangle"></i>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col-md-3 col-sm-6">
                    <div class="stats-card">
                        <div class="d-flex justify-content-between align-items-center">
                            <div>
                                <h3 class="mb-0">{{ formatCurrency(statistics.totalValue) }}</h3>
                                <p class="mb-0">Total Nilai</p>
                            </div>
                            <div class="fs-1 opacity-50">
                                <i class="fas fa-chart-line"></i>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Search and Filters -->
            <div class="card mb-4">
                <div class="card-body">
                    <div class="row g-3">
                        <div class="col-md-4">
                            <div class="search-container">
                                <label class="form-label">Pencarian</label>
                                <input 
                                    v-model="searchQuery" 
                                    type="text" 
                                    class="form-control"
                                    placeholder="Cari kode, nama, atau kategori..."
                                    @input="debouncedSearch"
                                >
                                <div v-if="isSearching" class="search-spinner">
                                    <div class="spinner-border spinner-border-sm text-primary" role="status">
                                        <span class="visually-hidden">Searching...</span>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="col-md-2">
                            <label class="form-label">Kategori</label>
                            <select v-model="filters.category" class="form-select" @change="applyFilters">
                                <option value="">Semua Kategori</option>
                                <option v-for="category in categories" :key="category" :value="category">
                                    {{ category }}
                                </option>
                            </select>
                        </div>
                        <div class="col-md-2">
                            <label class="form-label">Status Stok</label>
                            <select v-model="filters.stockStatus" class="form-select" @change="applyFilters">
                                <option value="">Semua Status</option>
                                <option value="high">Tersedia</option>
                                <option value="medium">Terbatas</option>
                                <option value="low">Rendah</option>
                            </select>
                        </div>
                        <div class="col-md-2">
                            <label class="form-label">Urutkan</label>
                            <select v-model="sortBy" class="form-select" @change="applyFilters">
                                <option value="name">Nama</option>
                                <option value="stock">Stok</option>
                                <option value="price">Harga</option>
                                <option value="category">Kategori</option>
                            </select>
                        </div>
                        <div class="col-md-2">
                            <label class="form-label">&nbsp;</label>
                            <div>
                                <button class="btn btn-outline-secondary w-100" @click="resetFilters">
                                    <i class="fas fa-redo me-1"></i>Reset
                                </button>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Data Table -->
            <div class="card">
                <div class="card-header d-flex justify-content-between align-items-center">
                    <h5 class="mb-0">
                        <i class="fas fa-list me-2"></i>Daftar Bahan Ajar
                        <span class="badge bg-secondary ms-2">{{ filteredItems.length }} items</span>
                    </h5>
                    <div class="btn-group" role="group">
                        <button 
                            type="button" 
                            class="btn btn-outline-secondary"
                            :class="{ active: viewMode === 'table' }"
                            @click="viewMode = 'table'"
                        >
                            <i class="fas fa-table"></i>
                        </button>
                        <button 
                            type="button" 
                            class="btn btn-outline-secondary"
                            :class="{ active: viewMode === 'grid' }"
                            @click="viewMode = 'grid'"
                        >
                            <i class="fas fa-th"></i>
                        </button>
                    </div>
                </div>
                <div class="card-body">
                    <!-- Loading State -->
                    <div v-if="isLoading" class="text-center py-5">
                        <div class="spinner-border text-primary" role="status">
                            <span class="visually-hidden">Loading...</span>
                        </div>
                        <p class="mt-2">Memuat data...</p>
                    </div>

                    <!-- Empty State -->
                    <div v-else-if="filteredItems.length === 0" class="text-center py-5">
                        <i class="fas fa-inbox fa-3x text-muted mb-3"></i>
                        <h5>Tidak ada data</h5>
                        <p class="text-muted">Tidak ada bahan ajar yang sesuai dengan filter yang dipilih.</p>
                        <button class="btn btn-primary" @click="resetFilters">Reset Filter</button>
                    </div>

                    <!-- Table View -->
                    <div v-else-if="viewMode === 'table'">
                        <div class="table-responsive">
                            <table class="table table-hover">
                                <thead>
                                    <tr>
                                        <th>Kode</th>
                                        <th>Nama Bahan Ajar</th>
                                        <th>Kategori</th>
                                        <th>Stok</th>
                                        <th>Harga</th>
                                        <th>Status</th>
                                        <th>Aksi</th>
                                    </tr>
                                </thead>
                                <tbody>
                                    <transition-group name="fade" tag="tbody">
                                        <tr v-for="item in paginatedItems" :key="item.id">
                                            <td>
                                                <code>{{ item.kode }}</code>
                                            </td>
                                            <td>
                                                <div class="d-flex align-items-center">
                                                    <img 
                                                        :src="item.gambar || 'https://picsum.photos/40/40'" 
                                                        class="rounded me-2" 
                                                        width="40" 
                                                        height="40"
                                                        :alt="item.nama"
                                                    >
                                                    <div>
                                                        <strong>{{ item.nama }}</strong>
                                                        <br><small class="text-muted">{{ item.deskripsi }}</small>
                                                    </div>
                                                </div>
                                            </td>
                                            <td>
                                                <span class="badge bg-info">{{ item.kategori }}</span>
                                            </td>
                                            <td>
                                                <div class="d-flex align-items-center">
                                                    <span class="me-2">{{ item.stok }}</span>
                                                    <div class="progress" style="width: 50px; height: 8px;">
                                                        <div 
                                                            class="progress-bar" 
                                                            :class="getStockProgressClass(item.stok)"
                                                            :style="{ width: getStockPercentage(item.stok) + '%' }"
                                                        ></div>
                                                    </div>
                                                </div>
                                            </td>
                                            <td>{{ formatCurrency(item.harga) }}</td>
                                            <td>
                                                <span class="badge stock-badge" :class="getStockBadgeClass(item.stok)">
                                                    {{ getStockStatus(item.stok) }}
                                                </span>
                                            </td>
                                            <td>
                                                <div class="btn-group" role="group">
                                                    <button 
                                                        class="btn btn-sm btn-outline-primary" 
                                                        @click="editItem(item)"
                                                        title="Edit"
                                                    >
                                                        <i class="fas fa-edit"></i>
                                                    </button>
                                                    <button 
                                                        class="btn btn-sm btn-outline-success" 
                                                        @click="adjustStock(item)"
                                                        title="Adjust Stock"
                                                    >
                                                        <i class="fas fa-plus-minus"></i>
                                                    </button>
                                                    <button 
                                                        class="btn btn-sm btn-outline-danger" 
                                                        @click="deleteItem(item)"
                                                        title="Delete"
                                                    >
                                                        <i class="fas fa-trash"></i>
                                                    </button>
                                                </div>
                                            </td>
                                        </tr>
                                    </transition-group>
                                </tbody>
                            </table>
                        </div>
                    </div>

                    <!-- Grid View -->
                    <div v-else class="row">
                        <transition-group name="slide" tag="div" class="row">
                            <div v-for="item in paginatedItems" :key="item.id" class="col-md-4 col-sm-6 mb-4">
                                <div class="card h-100">
                                    <img 
                                        :src="item.gambar || 'https://picsum.photos/300/200'" 
                                        class="card-img-top" 
                                        :alt="item.nama"
                                        style="height: 200px; object-fit: cover;"
                                    >
                                    <div class="card-body">
                                        <h6 class="card-title">{{ item.nama }}</h6>
                                        <p class="card-text text-muted small">{{ item.deskripsi }}</p>
                                        <div class="mb-2">
                                            <span class="badge bg-info me-1">{{ item.kategori }}</span>
                                            <span class="badge stock-badge" :class="getStockBadgeClass(item.stok)">
                                                {{ getStockStatus(item.stok) }}
                                            </span>
                                        </div>
                                        <div class="d-flex justify-content-between align-items-center">
                                            <div>
                                                <strong>{{ formatCurrency(item.harga) }}</strong>
                                                <br><small class="text-muted">Stok: {{ item.stok }}</small>
                                            </div>
                                            <div class="btn-group" role="group">
                                                <button 
                                                    class="btn btn-sm btn-outline-primary" 
                                                    @click="editItem(item)"
                                                >
                                                    <i class="fas fa-edit"></i>
                                                </button>
                                                <button 
                                                    class="btn btn-sm btn-outline-success" 
                                                    @click="adjustStock(item)"
                                                >
                                                    <i class="fas fa-plus-minus"></i>
                                                </button>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </transition-group>
                    </div>

                    <!-- Pagination -->
                    <nav v-if="totalPages > 1" class="mt-4">
                        <ul class="pagination justify-content-center">
                            <li class="page-item" :class="{ disabled: currentPage === 1 }">
                                <a class="page-link" href="#" @click.prevent="currentPage--">
                                    <i class="fas fa-chevron-left"></i>
                                </a>
                            </li>
                            <li 
                                v-for="page in visiblePages" 
                                :key="page" 
                                class="page-item" 
                                :class="{ active: currentPage === page }"
                            >
                                <a class="page-link" href="#" @click.prevent="currentPage = page">
                                    {{ page }}
                                </a>
                            </li>
                            <li class="page-item" :class="{ disabled: currentPage === totalPages }">
                                <a class="page-link" href="#" @click.prevent="currentPage++">
                                    <i class="fas fa-chevron-right"></i>
                                </a>
                            </li>
                        </ul>
                    </nav>
                </div>
            </div>
        </main>

        <!-- Add/Edit Modal -->
        <div v-if="showAddModal || showEditModal" class="modal fade show d-block" tabindex="-1">
            <div class="modal-dialog modal-lg">
                <div class="modal-content">
                    <div class="modal-header">
                        <h5 class="modal-title">
                            <i class="fas fa-plus me-2"></i>
                            {{ editingItem ? 'Edit' : 'Tambah' }} Bahan Ajar
                        </h5>
                        <button type="button" class="btn-close" @click="closeModals"></button>
                    </div>
                    <div class="modal-body">
                        <form @submit.prevent="saveItem">
                            <div class="row g-3">
                                <div class="col-md-6">
                                    <label class="form-label">Kode Bahan Ajar *</label>
                                    <input 
                                        v-model="formData.kode" 
                                        type="text" 
                                        class="form-control"
                                        :class="{ 'is-invalid': errors.kode }"
                                        required
                                    >
                                    <div v-if="errors.kode" class="invalid-feedback">
                                        {{ errors.kode }}
                                    </div>
                                </div>
                                <div class="col-md-6">
                                    <label class="form-label">Nama Bahan Ajar *</label>
                                    <input 
                                        v-model="formData.nama" 
                                        type="text" 
                                        class="form-control"
                                        :class="{ 'is-invalid': errors.nama }"
                                        required
                                    >
                                    <div v-if="errors.nama" class="invalid-feedback">
                                        {{ errors.nama }}
                                    </div>
                                </div>
                                <div class="col-md-6">
                                    <label class="form-label">Kategori *</label>
                                    <select 
                                        v-model="formData.kategori" 
                                        class="form-select"
                                        :class="{ 'is-invalid': errors.kategori }"
                                        required
                                    >
                                        <option value="">Pilih Kategori</option>
                                        <option v-for="category in categories" :key="category" :value="category">
                                            {{ category }}
                                        </option>
                                    </select>
                                    <div v-if="errors.kategori" class="invalid-feedback">
                                        {{ errors.kategori }}
                                    </div>
                                </div>
                                <div class="col-md-6">
                                    <label class="form-label">Stok *</label>
                                    <input 
                                        v-model.number="formData.stok" 
                                        type="number" 
                                        class="form-control"
                                        :class="{ 'is-invalid': errors.stok }"
                                        min="0"
                                        required
                                    >
                                    <div v-if="errors.stok" class="invalid-feedback">
                                        {{ errors.stok }}
                                    </div>
                                </div>
                                <div class="col-md-6">
                                    <label class="form-label">Harga *</label>
                                    <input 
                                        v-model.number="formData.harga" 
                                        type="number" 
                                        class="form-control"
                                        :class="{ 'is-invalid': errors.harga }"
                                        min="0"
                                        step="0.01"
                                        required
                                    >
                                    <div v-if="errors.harga" class="invalid-feedback">
                                        {{ errors.harga }}
                                    </div>
                                </div>
                                <div class="col-md-6">
                                    <label class="form-label">Gambar URL</label>
                                    <input 
                                        v-model="formData.gambar" 
                                        type="url" 
                                        class="form-control"
                                        placeholder="https://example.com/image.jpg"
                                    >
                                </div>
                                <div class="col-12">
                                    <label class="form-label">Deskripsi</label>
                                    <textarea 
                                        v-model="formData.deskripsi" 
                                        class="form-control"
                                        rows="3"
                                        placeholder="Deskripsi bahan ajar..."
                                    ></textarea>
                                </div>
                            </div>
                        </form>
                    </div>
                    <div class="modal-footer">
                        <button type="button" class="btn btn-secondary" @click="closeModals">Batal</button>
                        <button type="button" class="btn btn-primary" @click="saveItem">
                            <i class="fas fa-save me-1"></i>
                            {{ editingItem ? 'Update' : 'Simpan' }}
                        </button>
                    </div>
                </div>
            </div>
        </div>

        <!-- Stock Adjustment Modal -->
        <div v-if="showStockModal" class="modal fade show d-block" tabindex="-1">
            <div class="modal-dialog">
                <div class="modal-content">
                    <div class="modal-header">
                        <h5 class="modal-title">
                            <i class="fas fa-plus-minus me-2"></i>
                            Penyesuaian Stok
                        </h5>
                        <button type="button" class="btn-close" @click="showStockModal = false"></button>
                    </div>
                    <div class="modal-body">
                        <div class="mb-3">
                            <label class="form-label">Bahan Ajar</label>
                            <input 
                                type="text" 
                                class="form-control" 
                                :value="stockAdjustment.item?.nama" 
                                readonly
                            >
                        </div>
                        <div class="mb-3">
                            <label class="form-label">Stok Saat Ini</label>
                            <input 
                                type="number" 
                                class="form-control" 
                                :value="stockAdjustment.item?.stok" 
                                readonly
                            >
                        </div>
                        <div class="mb-3">
                            <label class="form-label">Jenis Penyesuaian</label>
                            <select v-model="stockAdjustment.type" class="form-select">
                                <option value="add">Tambah Stok</option>
                                <option value="subtract">Kurangi Stok</option>
                                <option value="set">Set Stok</option>
                            </select>
                        </div>
                        <div class="mb-3">
                            <label class="form-label">Jumlah</label>
                            <input 
                                v-model.number="stockAdjustment.amount" 
                                type="number" 
                                class="form-control"
                                min="0"
                                required
                            >
                        </div>
                        <div class="mb-3">
                            <label class="form-label">Alasan</label>
                            <textarea 
                                v-model="stockAdjustment.reason" 
                                class="form-control"
                                rows="2"
                                placeholder="Alasan penyesuaian stok..."
                            ></textarea>
                        </div>
                    </div>
                    <div class="modal-footer">
                        <button type="button" class="btn btn-secondary" @click="showStockModal = false">Batal</button>
                        <button type="button" class="btn btn-primary" @click="saveStockAdjustment">
                            <i class="fas fa-save me-1"></i>Simpan
                        </button>
                    </div>
                </div>
            </div>
        </div>

        <!-- Notifications -->
        <transition-group name="fade" tag="div" class="notification-container">
            <div 
                v-for="notification in notifications" 
                :key="notification.id"
                class="alert alert-dismissible fade show"
                :class="'alert-' + notification.type"
                role="alert"
            >
                <div class="d-flex align-items-center">
                    <i :class="getNotificationIcon(notification.type)" class="me-2"></i>
                    <div>
                        <strong>{{ notification.title }}</strong>
                        <br>{{ notification.message }}
                    </div>
                </div>
                <button type="button" class="btn-close" @click="removeNotification(notification.id)"></button>
            </div>
        </transition-group>

        <!-- Loading Overlay -->
        <div v-if="isProcessing" class="loading-overlay">
            <div class="text-center">
                <div class="spinner-border text-primary" role="status">
                    <span class="visually-hidden">Processing...</span>
                </div>
                <p class="mt-2">{{ processingMessage }}</p>
            </div>
        </div>
    </div>

    <!-- Bootstrap JS -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
    <!-- Vue.js -->
    <script src="https://cdn.jsdelivr.net/npm/vue@2.6.14/dist/vue.js"></script>
    <!-- Custom JS -->
    <script src="js/app.js"></script>
</body>
</html>
```

---

## 📱 **JavaScript Implementation - js/app.js**

```javascript
// ===================================
// SITTA Stock Management Application
// Vue.js Implementation
// ===================================

// Main Vue Application
new Vue({
    el: '#app',
    
    // Data Properties
    data: {
        // User data
        currentUser: {
            id: 1,
            name: 'Admin SITTA',
            email: 'admin@ut.ac.id',
            role: 'admin'
        },
        
        // Application state
        isLoading: true,
        isSearching: false,
        isProcessing: false,
        processingMessage: '',
        
        // Data
        items: [],
        categories: [],
        
        // UI State
        viewMode: 'table', // 'table' or 'grid'
        showAddModal: false,
        showEditModal: false,
        showStockModal: false,
        
        // Forms
        formData: {
            kode: '',
            nama: '',
            kategori: '',
            stok: 0,
            harga: 0,
            gambar: '',
            deskripsi: ''
        },
        
        editingItem: null,
        stockAdjustment: {
            item: null,
            type: 'add',
            amount: 0,
            reason: ''
        },
        
        // Filters and Search
        searchQuery: '',
        filters: {
            category: '',
            stockStatus: ''
        },
        sortBy: 'name',
        currentPage: 1,
        itemsPerPage: 10,
        
        // Validation
        errors: {},
        
        // Notifications
        notifications: [],
        notificationId: 1,
        
        // Debounce timer
        searchTimeout: null
    },
    
    // Computed Properties
    computed: {
        // Statistics
        statistics() {
            return {
                totalItems: this.items.length,
                totalStock: this.items.reduce((sum, item) => sum + item.stok, 0),
                lowStockItems: this.items.filter(item => item.stok < 10).length,
                totalValue: this.items.reduce((sum, item) => sum + (item.stok * item.harga), 0)
            };
        },
        
        // Filtered items
        filteredItems() {
            let result = [...this.items];
            
            // Search filter
            if (this.searchQuery) {
                const query = this.searchQuery.toLowerCase();
                result = result.filter(item => 
                    item.kode.toLowerCase().includes(query) ||
                    item.nama.toLowerCase().includes(query) ||
                    item.kategori.toLowerCase().includes(query) ||
                    item.deskripsi.toLowerCase().includes(query)
                );
            }
            
            // Category filter
            if (this.filters.category) {
                result = result.filter(item => item.kategori === this.filters.category);
            }
            
            // Stock status filter
            if (this.filters.stockStatus) {
                result = result.filter(item => this.getStockStatus(item.stok) === this.filters.stockStatus);
            }
            
            // Sorting
            result.sort((a, b) => {
                switch (this.sortBy) {
                    case 'name':
                        return a.nama.localeCompare(b.nama);
                    case 'stock':
                        return b.stok - a.stok;
                    case 'price':
                        return a.harga - b.harga;
                    case 'category':
                        return a.kategori.localeCompare(b.kategori);
                    default:
                        return 0;
                }
            });
            
            return result;
        },
        
        // Pagination
        totalPages() {
            return Math.ceil(this.filteredItems.length / this.itemsPerPage);
        },
        
        paginatedItems() {
            const start = (this.currentPage - 1) * this.itemsPerPage;
            const end = start + this.itemsPerPage;
            return this.filteredItems.slice(start, end);
        },
        
        visiblePages() {
            const pages = [];
            const maxVisible = 5;
            const half = Math.floor(maxVisible / 2);
            
            let start = Math.max(1, this.currentPage - half);
            let end = Math.min(this.totalPages, start + maxVisible - 1);
            
            if (end - start + 1 < maxVisible) {
                start = Math.max(1, end - maxVisible + 1);
            }
            
            for (let i = start; i <= end; i++) {
                pages.push(i);
            }
            
            return pages;
        }
    },
    
    // Methods
    methods: {
        // Data Management
        async loadData() {
            try {
                this.isLoading = true;
                
                // Simulate API call
                const response = await this.mockApiCall('/api/bahan-ajar', 'GET');
                this.items = response.data;
                
                // Extract categories
                this.categories = [...new Set(this.items.map(item => item.kategori))];
                
                this.showNotification('success', 'Berhasil', 'Data berhasil dimuat');
                
            } catch (error) {
                console.error('Error loading data:', error);
                this.showNotification('error', 'Error', 'Gagal memuat data');
            } finally {
                this.isLoading = false;
            }
        },
        
        // CRUD Operations
        async saveItem() {
            if (!this.validateForm()) return;
            
            try {
                this.isProcessing = true;
                this.processingMessage = this.editingItem ? 'Mengupdate data...' : 'Menyimpan data...';
                
                const itemData = { ...this.formData };
                
                if (this.editingItem) {
                    // Update existing item
                    const response = await this.mockApiCall(`/api/bahan-ajar/${this.editingItem.id}`, 'PUT', itemData);
                    const index = this.items.findIndex(item => item.id === this.editingItem.id);
                    this.$set(this.items, index, response.data);
                    this.showNotification('success', 'Berhasil', 'Data berhasil diupdate');
                } else {
                    // Add new item
                    const response = await this.mockApiCall('/api/bahan-ajar', 'POST', itemData);
                    this.items.push(response.data);
                    this.showNotification('success', 'Berhasil', 'Data berhasil ditambahkan');
                }
                
                this.closeModals();
                
            } catch (error) {
                console.error('Error saving item:', error);
                this.showNotification('error', 'Error', 'Gagal menyimpan data');
            } finally {
                this.isProcessing = false;
            }
        },
        
        async deleteItem(item) {
            if (!confirm(`Apakah Anda yakin ingin menghapus "${item.nama}"?`)) return;
            
            try {
                this.isProcessing = true;
                this.processingMessage = 'Menghapus data...';
                
                await this.mockApiCall(`/api/bahan-ajar/${item.id}`, 'DELETE');
                
                const index = this.items.findIndex(i => i.id === item.id);
                this.items.splice(index, 1);
                
                this.showNotification('success', 'Berhasil', 'Data berhasil dihapus');
                
            } catch (error) {
                console.error('Error deleting item:', error);
                this.showNotification('error', 'Error', 'Gagal menghapus data');
            } finally {
                this.isProcessing = false;
            }
        },
        
        async saveStockAdjustment() {
            if (!this.stockAdjustment.amount || this.stockAdjustment.amount <= 0) {
                this.showNotification('warning', 'Peringatan', 'Jumlah penyesuaian harus lebih dari 0');
                return;
            }
            
            try {
                this.isProcessing = true;
                this.processingMessage = 'Menyesuaikan stok...';
                
                const adjustmentData = {
                    itemId: this.stockAdjustment.item.id,
                    type: this.stockAdjustment.type,
                    amount: this.stockAdjustment.amount,
                    reason: this.stockAdjustment.reason
                };
                
                const response = await this.mockApiCall('/api/stock-adjustment', 'POST', adjustmentData);
                
                // Update item stock
                const item = this.items.find(i => i.id === this.stockAdjustment.item.id);
                item.stok = response.data.newStock;
                
                this.showNotification('success', 'Berhasil', 'Stok berhasil disesuaikan');
                this.showStockModal = false;
                
            } catch (error) {
                console.error('Error adjusting stock:', error);
                this.showNotification('error', 'Error', 'Gagal menyesuaikan stok');
            } finally {
                this.isProcessing = false;
            }
        },
        
        // UI Methods
        editItem(item) {
            this.editingItem = item;
            this.formData = { ...item };
            this.showEditModal = true;
        },
        
        adjustStock(item) {
            this.stockAdjustment.item = item;
            this.stockAdjustment.type = 'add';
            this.stockAdjustment.amount = 0;
            this.stockAdjustment.reason = '';
            this.showStockModal = true;
        },
        
        closeModals() {
            this.showAddModal = false;
            this.showEditModal = false;
            this.showStockModal = false;
            this.editingItem = null;
            this.resetForm();
            this.errors = {};
        },
        
        // Search and Filters
        debouncedSearch() {
            this.isSearching = true;
            
            if (this.searchTimeout) {
                clearTimeout(this.searchTimeout);
            }
            
            this.searchTimeout = setTimeout(() => {
                this.applyFilters();
                this.isSearching = false;
            }, 500);
        },
        
        applyFilters() {
            this.currentPage = 1;
        },
        
        resetFilters() {
            this.searchQuery = '';
            this.filters = {
                category: '',
                stockStatus: ''
            };
            this.sortBy = 'name';
            this.currentPage = 1;
        },
        
        // Utility Methods
        validateForm() {
            this.errors = {};
            
            if (!this.formData.kode.trim()) {
                this.errors.kode = 'Kode bahan ajar harus diisi';
            }
            
            if (!this.formData.nama.trim()) {
                this.errors.nama = 'Nama bahan ajar harus diisi';
            }
            
            if (!this.formData.kategori) {
                this.errors.kategori = 'Kategori harus dipilih';
            }
            
            if (this.formData.stok < 0) {
                this.errors.stok = 'Stok tidak boleh negatif';
            }
            
            if (this.formData.harga < 0) {
                this.errors.harga = 'Harga tidak boleh negatif';
            }
            
            // Check for duplicate kode (except when editing)
            const duplicate = this.items.find(item => 
                item.kode === this.formData.kode && item.id !== this.editingItem?.id
            );
            if (duplicate) {
                this.errors.kode = 'Kode bahan ajar sudah ada';
            }
            
            return Object.keys(this.errors).length === 0;
        },
        
        resetForm() {
            this.formData = {
                kode: '',
                nama: '',
                kategori: '',
                stok: 0,
                harga: 0,
                gambar: '',
                deskripsi: ''
            };
        },
        
        // Stock Status Methods
        getStockStatus(stock) {
            if (stock === 0) return 'empty';
            if (stock < 10) return 'low';
            if (stock < 50) return 'medium';
            return 'high';
        },
        
        getStockBadgeClass(stock) {
            const status = this.getStockStatus(stock);
            return `stock-${status}`;
        },
        
        getStockProgressClass(stock) {
            const status = this.getStockStatus(stock);
            const classes = {
                'empty': 'bg-danger',
                'low': 'bg-warning',
                'medium': 'bg-info',
                'high': 'bg-success'
            };
            return classes[status] || 'bg-secondary';
        },
        
        getStockPercentage(stock) {
            return Math.min(100, (stock / 100) * 100);
        },
        
        // Notification Methods
        showNotification(type, title, message) {
            const notification = {
                id: this.notificationId++,
                type,
                title,
                message,
                timestamp: new Date()
            };
            
            this.notifications.push(notification);
            
            // Auto remove after 5 seconds
            setTimeout(() => {
                this.removeNotification(notification.id);
            }, 5000);
        },
        
        removeNotification(id) {
            const index = this.notifications.findIndex(n => n.id === id);
            if (index > -1) {
                this.notifications.splice(index, 1);
            }
        },
        
        getNotificationIcon(type) {
            const icons = {
                'success': 'fas fa-check-circle',
                'error': 'fas fa-exclamation-circle',
                'warning': 'fas fa-exclamation-triangle',
                'info': 'fas fa-info-circle'
            };
            return icons[type] || 'fas fa-info-circle';
        },
        
        // Utility Functions
        formatCurrency(amount) {
            return new Intl.NumberFormat('id-ID', {
                style: 'currency',
                currency: 'IDR',
                minimumFractionDigits: 0
            }).format(amount);
        },
        
        // Export Data
        exportData() {
            try {
                this.isProcessing = true;
                this.processingMessage = 'Mengekspor data...';
                
                // Create CSV content
                const headers = ['Kode', 'Nama', 'Kategori', 'Stok', 'Harga', 'Status'];
                const rows = this.filteredItems.map(item => [
                    item.kode,
                    item.nama,
                    item.kategori,
                    item.stok,
                    item.harga,
                    this.getStockStatus(item.stok)
                ]);
                
                const csvContent = [headers, ...rows]
                    .map(row => row.map(cell => `"${cell}"`).join(','))
                    .join('\n');
                
                // Download CSV file
                const blob = new Blob([csvContent], { type: 'text/csv' });
                const url = window.URL.createObjectURL(blob);
                const a = document.createElement('a');
                a.href = url;
                a.download = `sitta-stock-${new Date().toISOString().split('T')[0]}.csv`;
                a.click();
                window.URL.revokeObjectURL(url);
                
                this.showNotification('success', 'Berhasil', 'Data berhasil diekspor');
                
            } catch (error) {
                console.error('Error exporting data:', error);
                this.showNotification('error', 'Error', 'Gagal mengekspor data');
            } finally {
                this.isProcessing = false;
            }
        },
        
        // Mock API
        async mockApiCall(endpoint, method = 'GET', data = null) {
            // Simulate network delay
            await new Promise(resolve => setTimeout(resolve, 800 + Math.random() * 1200));
            
            // Simulate API responses
            if (endpoint === '/api/bahan-ajar' && method === 'GET') {
                return {
                    success: true,
                    data: this.getMockData()
                };
            }
            
            if (method === 'POST' && endpoint === '/api/bahan-ajar') {
                const newItem = {
                    ...data,
                    id: Date.now(),
                    createdAt: new Date().toISOString()
                };
                return { success: true, data: newItem };
            }
            
            if (method === 'PUT' && endpoint.startsWith('/api/bahan-ajar/')) {
                return { success: true, data: { ...data, updatedAt: new Date().toISOString() } };
            }
            
            if (method === 'DELETE' && endpoint.startsWith('/api/bahan-ajar/')) {
                return { success: true };
            }
            
            if (method === 'POST' && endpoint === '/api/stock-adjustment') {
                const { itemId, type, amount } = data;
                const item = this.items.find(i => i.id === itemId);
                let newStock = item.stok;
                
                if (type === 'add') newStock += amount;
                else if (type === 'subtract') newStock = Math.max(0, newStock - amount);
                else if (type === 'set') newStock = amount;
                
                return { success: true, data: { newStock } };
            }
            
            // Simulate random errors
            if (Math.random() < 0.1) {
                throw new Error('Simulated API error');
            }
            
            return { success: true };
        },
        
        getMockData() {
            return [
                {
                    id: 1,
                    kode: 'BA001',
                    nama: 'Pengantar Ilmu Komunikasi',
                    kategori: 'Buku',
                    stok: 45,
                    harga: 85000,
                    gambar: 'https://picsum.photos/300/200?random=1',
                    deskripsi: 'Buku pengantar untuk mahasiswa baru ilmu komunikasi'
                },
                {
                    id: 2,
                    kode: 'BA002',
                    nama: 'Manajemen Keuangan',
                    kategori: 'Buku',
                    stok: 23,
                    harga: 95000,
                    gambar: 'https://picsum.photos/300/200?random=2',
                    deskripsi: 'Buku manajemen keuangan untuk semester 3'
                },
                {
                    id: 3,
                    kode: 'VD001',
                    nama: 'Video Tutorial Web Development',
                    kategori: 'Video',
                    stok: 100,
                    harga: 150000,
                    gambar: 'https://picsum.photos/300/200?random=3',
                    deskripsi: 'Video tutorial lengkap web development dengan HTML, CSS, JavaScript'
                },
                {
                    id: 4,
                    kode: 'SW001',
                    nama: 'Software Simulasi Bisnis',
                    kategori: 'Software',
                    stok: 8,
                    harga: 450000,
                    gambar: 'https://picsum.photos/300/200?random=4',
                    deskripsi: 'Software simulasi untuk praktikum manajemen'
                },
                {
                    id: 5,
                    kode: 'BA003',
                    nama: 'Kepemimpinan Organisasi',
                    kategori: 'Buku',
                    stok: 67,
                    harga: 78000,
                    gambar: 'https://picsum.photos/300/200?random=5',
                    deskripsi: 'Buku tentang teori dan praktik kepemimpinan'
                },
                {
                    id: 6,
                    kode: 'VD002',
                    nama: 'Video Pembelajaran Matematika Dasar',
                    kategori: 'Video',
                    stok: 5,
                    harga: 120000,
                    gambar: 'https://picsum.photos/300/200?random=6',
                    deskripsi: 'Video pembelajaran matematika untuk tingkat dasar'
                }
            ];
        }
    },
    
    // Watchers
    watch: {
        // Watch for page changes
        currentPage(newPage) {
            // Scroll to top when page changes
            window.scrollTo({ top: 0, behavior: 'smooth' });
        },
        
        // Watch for low stock items
        'statistics.lowStockItems'(newCount) {
            if (newCount > 0) {
                this.showNotification('warning', 'Peringatan Stok', `${newCount} item dengan stok rendah`);
            }
        }
    },
    
    // Lifecycle Hooks
    async created() {
        await this.loadData();
    },
    
    mounted() {
        // Initialize tooltips and other Bootstrap components
        console.log('SITTA Stock Management Application mounted');
    },
    
    beforeDestroy() {
        // Cleanup timeouts
        if (this.searchTimeout) {
            clearTimeout(this.searchTimeout);
        }
    }
});
```

---

## 🎯 **Key Features Implemented**

### ✅ **Core Functionality**
- **CRUD Operations**: Create, Read, Update, Delete bahan ajar
- **Real-time Search**: Debounced search dengan loading states
- **Advanced Filtering**: Category, stock status, sorting
- **Pagination**: Efficient data pagination
- **Stock Management**: Adjust stock dengan tracking
- **Data Export**: CSV export functionality

### ✅ **Vue.js Features Demonstrated**
- **Data Binding**: Two-way binding pada forms
- **Computed Properties**: Statistics, filtering, pagination
- **Watchers**: Stock monitoring, search debouncing
- **Conditional Rendering**: Dynamic UI berdasarkan state
- **Component Lifecycle**: Proper initialization dan cleanup
- **Event Handling**: User interactions dan form submissions
- **Transitions**: Smooth animations dan transitions

### ✅ **User Experience**
- **Responsive Design**: Mobile-friendly interface
- **Loading States**: Visual feedback untuk async operations
- **Error Handling**: Comprehensive error management
- **Notifications**: Real-time feedback system
- **Accessibility**: Proper ARIA labels dan semantic HTML
- **Performance**: Optimized rendering dan debouncing

---

**🎉 Complete SITTA Stock Application Ready!**

**📝 Implementation Highlights:**
1. **Full-featured CRUD** dengan validation
2. **Advanced search & filtering** system
3. **Real-time stock management**
4. **Responsive grid/table views**
5. **Data export functionality**
6. **Comprehensive error handling**
7. **Professional UI/UX design**

**🚀 Ready for Production Deployment!**

---

## 🐛 **Debugging Guide & Performance Optimization**

### 🔍 **Vue.js Debugging Techniques**

#### **1. Vue DevTools Installation & Usage**

**📦 Installation:**
```bash
# Chrome/Edge
https://chrome.google.com/webstore/detail/vuejs-devtools/

# Firefox
https://addons.mozilla.org/en-US/firefox/addon/vue-js-devtools/

# Safari
https://github.com/vuejs/vue-devtools/tree/main/packages/shell-chrome
```

**🛠️ DevTools Features:**
- **🔍 Component Inspection**: View component hierarchy and state
- **📊 Vuex State Management**: Monitor state changes
- **⏡ Performance Profiling**: Identify performance bottlenecks
- **🐛 Time-travel Debugging**: Step through state changes
- **📱 Event Tracking**: Monitor event emissions

#### **2. Console Debugging Techniques**

```javascript
// 🔍 Debug Vue instance
console.log('Vue instance:', this.$data);
console.log('Computed properties:', this.$options.computed);
console.log('Methods:', this.$options.methods);

// 🔍 Debug reactivity
this.$watch('someData', (newVal, oldVal) => {
    console.log('Data changed:', { newVal, oldVal });
});

// 🔍 Debug component lifecycle
const originalCreated = this.$options.created;
this.$options.created = function() {
    console.log('Component created:', this.$options.name);
    originalCreated.call(this);
};

// 🔍 Debug event handling
methods: {
    handleClick(event) {
        console.log('Click event:', event);
        console.log('Component data:', this.$data);
        // Original logic here
    }
}
```

#### **3. Common Debugging Scenarios**

```javascript
// 🐛 Scenario 1: Data not updating
// Problem: Direct property addition
this.newProperty = 'value'; // ❌ Not reactive

// Solution: Use Vue.set
this.$set(this, 'newProperty', 'value'); // ✅ Reactive

// 🐛 Scenario 2: Array mutation not triggering updates
// Problem: Direct index assignment
this.items[0] = newItem; // ❌ Not reactive

// Solution: Use Vue.set or array methods
this.$set(this.items, 0, newItem); // ✅ Reactive
this.items.splice(0, 1, newItem); // ✅ Reactive

// 🐛 Scenario 3: Computed property not updating
// Problem: Computed depends on non-reactive data
computed: {
    fullName() {
        return this.firstName + ' ' + this.lastName; // ❌ If properties not in data
    }
}

// Solution: Ensure dependencies are in data
data() {
    return {
        firstName: '',
        lastName: '' // ✅ Reactive dependencies
    };
}
```

---

## ⚡ **Performance Optimization Strategies**

### 🎯 **Rendering Performance**

#### **1. Optimize List Rendering**

```javascript
// ❌ BAD: Inefficient key usage
<div v-for="item in items" :key="item.id">
    {{ item.name }}
</div>

// ✅ GOOD: Stable unique keys
<div v-for="item in items" :key="item.id">
    {{ item.name }}
</div>

// ✅ BETTER: Use v-show for frequently toggled lists
<div v-show="showList">
    <div v-for="item in items" :key="item.id">
        {{ item.name }}
    </div>
</div>

// ❌ AVOID: Complex computations in template
<div v-for="item in items.filter(i => i.active).sort((a, b) => a.name.localeCompare(b.name))">
    {{ item.name }}
</div>

// ✅ BETTER: Use computed properties
computed: {
    filteredAndSortedItems() {
        return this.items
            .filter(item => item.active)
            .sort((a, b) => a.name.localeCompare(b.name));
    }
}
```

#### **2. Optimize Computed Properties**

```javascript
// ❌ BAD: Expensive repeated calculations
computed: {
    expensiveResult() {
        // This runs every time, even if dependencies haven't changed meaningfully
        return this.items.reduce((sum, item) => {
            // Complex calculation
            return sum + this.calculateComplexValue(item);
        }, 0);
    }
}

// ✅ GOOD: Memoization and dependency optimization
computed: {
    expensiveResult() {
        // Only recalculate when items actually change
        if (!this._cachedResult || this._itemsVersion !== this.items.length) {
            this._cachedResult = this.items.reduce((sum, item) => {
                return sum + this.calculateComplexValue(item);
            }, 0);
            this._itemsVersion = this.items.length;
        }
        return this._cachedResult;
    }
}
```

#### **3. Debounce and Throttle**

```javascript
// ✅ Debounced search
methods: {
    search: _.debounce(function(query) {
        // API call only after user stops typing
        this.performSearch(query);
    }, 300),
    
    // Custom debounce implementation
    debounce(func, wait) {
        let timeout;
        return function executedFunction(...args) {
            const later = () => {
                clearTimeout(timeout);
                func(...args);
            };
            clearTimeout(timeout);
            timeout = setTimeout(later, wait);
        };
    }
},

// ✅ Throttled scroll events
mounted() {
    window.addEventListener('scroll', this.throttledScroll);
},

methods: {
    throttledScroll: _.throttle(function() {
        this.updateScrollPosition();
    }, 100),
    
    beforeDestroy() {
        window.removeEventListener('scroll', this.throttledScroll);
    }
}
```

### 🧠 **Memory Management**

#### **1. Proper Cleanup**

```javascript
// ✅ Proper component cleanup
beforeDestroy() {
    // Clear timeouts
    if (this.searchTimeout) {
        clearTimeout(this.searchTimeout);
    }
    
    // Clear intervals
    if (this.updateInterval) {
        clearInterval(this.updateInterval);
    }
    
    // Remove event listeners
    window.removeEventListener('resize', this.handleResize);
    document.removeEventListener('click', this.handleDocumentClick);
    
    // Destroy third-party instances
    if (this.chartInstance) {
        this.chartInstance.destroy();
    }
    
    // Cancel pending requests
    if (this.pendingRequest) {
        this.pendingRequest.cancel();
    }
}
```

#### **2. Avoid Memory Leaks**

```javascript
// ❌ BAD: Creating objects without cleanup
methods: {
    loadData() {
        this.largeArray = new Array(100000).fill(0); // Memory leak
    }
}

// ✅ GOOD: Proper memory management
methods: {
    loadData() {
        // Use pagination or virtual scrolling for large datasets
        this.loadPage(1);
    },
    
    loadPage(page) {
        // Load only what's needed
        const pageSize = 100;
        const start = (page - 1) * pageSize;
        const end = start + pageSize;
        
        this.currentPageData = this.allData.slice(start, end);
    }
}
```

---

## 📋 **Best Practices Summary**

### 🎯 **Code Organization**

```javascript
// ✅ GOOD: Component-based architecture
components/
├── BaseButton.vue
├── BaseInput.vue
├── ProductCard.vue
└── DataTable.vue

// ✅ GOOD: Consistent naming conventions
methods: {
    // Use descriptive verb-noun patterns
    fetchUserData(),
    validateFormInput(),
    calculateTotalPrice(),
    
    // Event handlers start with 'handle'
    handleSubmit(),
    handleButtonClick(),
    handleInputChange()
}

// ✅ GOOD: Logical grouping
data() {
    return {
        // UI state
        isLoading: false,
        showModal: false,
        
        // Form data
        formData: {
            name: '',
            email: ''
        },
        
        // Application data
        users: [],
        products: []
    };
}
```

### 🔒 **Security Best Practices**

```javascript
// ✅ Input sanitization
methods: {
    sanitizeInput(input) {
        return input
            .trim()
            .replace(/<script\b[^<]*(?:(?!<\/script>)<[^<]*)*<\/script>/gi, '')
            .replace(/javascript:/gi, '');
    },
    
    handleUserInput(input) {
        const sanitized = this.sanitizeInput(input);
        this.userInput = sanitized;
    }
}

// ✅ XSS prevention
// Use v-text instead of v-html for user content
<div v-text="userContent"></div>

// If v-html is necessary, sanitize first
<div v-html="sanitizedHtml"></div>

computed: {
    sanitizedHtml() {
        return DOMPurify.sanitize(this.userContent);
    }
}
```

### ♿ **Accessibility Best Practices**

```html
<!-- ✅ Semantic HTML with proper ARIA labels -->
<button 
    @click="submitForm"
    :disabled="isSubmitting"
    aria-label="Submit form"
    aria-describedby="form-help"
>
    Submit
</button>

<div id="form-help" class="sr-only">
    Press Enter or Space to submit the form
</div>

<!-- ✅ Form accessibility -->
<form @submit.prevent="handleSubmit">
    <label for="username">Username:</label>
    <input 
        id="username"
        v-model="form.username"
        type="text"
        required
        aria-describedby="username-error"
        :aria-invalid="errors.username ? 'true' : 'false'"
    >
    <div 
        v-if="errors.username" 
        id="username-error"
        role="alert"
        class="error-message"
    >
        {{ errors.username }}
    </div>
</form>

<!-- ✅ Keyboard navigation -->
<div 
    tabindex="0"
    @keydown="handleKeydown"
    @click="handleClick"
    role="button"
    aria-label="Interactive element"
>
    Content
</div>
```

### 📱 **Responsive Design**

```css
/* ✅ Mobile-first CSS */
.container {
    padding: 1rem;
}

@media (min-width: 768px) {
    .container {
        padding: 2rem;
    }
}

@media (min-width: 1024px) {
    .container {
        max-width: 1200px;
        margin: 0 auto;
    }
}
```

```javascript
// ✅ Responsive Vue.js patterns
computed: {
    isMobile() {
        return this.windowWidth < 768;
    },
    
    isTablet() {
        return this.windowWidth >= 768 && this.windowWidth < 1024;
    },
    
    isDesktop() {
        return this.windowWidth >= 1024;
    }
},

mounted() {
    this.updateWindowWidth();
    window.addEventListener('resize', this.updateWindowWidth);
},

methods: {
    updateWindowWidth() {
        this.windowWidth = window.innerWidth;
    }
}
```

### 🧪 **Testing Strategies**

```javascript
// ✅ Component testing example
import { mount } from '@vue/test-utils';
import MyComponent from '@/components/MyComponent.vue';

describe('MyComponent', () => {
    test('renders correctly', () => {
        const wrapper = mount(MyComponent, {
            propsData: {
                title: 'Test Title'
            }
        });
        
        expect(wrapper.find('h1').text()).toBe('Test Title');
    });
    
    test('emits event on button click', async () => {
        const wrapper = mount(MyComponent);
        
        await wrapper.find('button').trigger('click');
        
        expect(wrapper.emitted().buttonClick).toBeTruthy();
    });
});
```

---

## 🎯 **Performance Checklist**

### ✅ **Before Production**

- [ ] **Remove console.log statements**
- [ ] **Optimize images and assets**
- [ ] **Enable code splitting**
- [ ] **Implement lazy loading**
- [ ] **Add error boundaries**
- [ ] **Optimize bundle size**
- [ ] **Enable caching strategies**
- [ ] **Test on multiple devices**
- [ ] **Validate HTML accessibility**
- [ ] **Check for memory leaks**

### 📊 **Performance Metrics**

```javascript
// ✅ Performance monitoring
const observer = new PerformanceObserver((list) => {
    for (const entry of list.getEntries()) {
        if (entry.entryType === 'measure') {
            console.log(`${entry.name}: ${entry.duration}ms`);
        }
    }
});

observer.observe({ entryTypes: ['measure'] });

// Measure component render time
methods: {
    async loadData() {
        performance.mark('load-start');
        
        await this.fetchData();
        
        performance.mark('load-end');
        performance.measure('load-duration', 'load-start', 'load-end');
    }
}
```

---

## 🚀 **Production Deployment Tips**

### 📦 **Build Optimization**

```javascript
// vue.config.js
module.exports = {
    productionSourceMap: false,
    
    configureWebpack: {
        optimization: {
            splitChunks: {
                chunks: 'all',
                maxSize: 244 * 1024, // 244KB
            }
        }
    },
    
    chainWebpack: (config) => {
        // Remove unused CSS
        config.plugin('purgecss').tap(args => {
            args[0].paths = ['./src/**/*.vue'];
            return args;
        });
    }
}
```

### 🔧 **Environment Configuration**

```javascript
// .env.production
VUE_APP_API_BASE_URL=https://api.sitta.ut.ac.id
VUE_APP_SENTRY_DSN=your-sentry-dsn
VUE_APP_GOOGLE_ANALYTICS_ID=GA-XXXXXXXXX

// src/config/index.js
export const config = {
    apiBaseUrl: process.env.VUE_APP_API_BASE_URL,
    isProduction: process.env.NODE_ENV === 'production',
    version: process.env.VUE_APP_VERSION
};
```

---

**🎉 Materi TUWeb 2 - Pertemuan 10 Enhancement Complete!**

**📝 Summary of Enhancements:**
1. ✅ **Comprehensive learning objectives** dengan competency breakdowns
2. ✅ **Detailed Vue.js fundamentals** dengan best practices
3. ✅ **Advanced data binding** dengan performance optimization
4. ✅ **Complex conditional rendering** dengan dynamic components
5. ✅ **Smart computed properties** dengan caching strategies
6. ✅ **Advanced watchers** dengan async operations
7. ✅ **Complete SITTA case study** dengan production-ready implementation
8. ✅ **Comprehensive debugging guide** dan performance optimization
9. ✅ **Best practices summary** untuk production deployment

**🚀 Ready for University Teaching!**
            methods: {
                goToStok() {
                    window.location.href = 'stok.html';
                }
            }
        });
    </script>
</body>
</html>
```

### 📄 **stok.html**
```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Stok Bahan Ajar - SITTA</title>
    <link rel="stylesheet" href="css/style.css">
    <script src="https://cdn.jsdelivr.net/npm/vue@2.6.14/dist/vue.js"></script>
</head>
<body>
    <div id="stok-app">
        <header class="header">
            <div class="container">
                <h1 class="logo">📚 SITTA</h1>
                <p class="subtitle">Stok Bahan Ajar</p>
            </div>
        </header>
        
        <nav class="navigation">
            <div class="container">
                <ul>
                    <li><a href="index.html" class="nav-link">🏠 Beranda</a></li>
                    <li><a href="stok.html" class="nav-link active">📦 Stok Bahan Ajar</a></li>
                    <li><a href="tracking.html" class="nav-link">📍 Tracking Pesanan</a></li>
                </ul>
            </div>
        </nav>
        
        <main class="main-content">
            <div class="container">
                <!-- Filter dan Search -->
                <section class="filter-section">
                    <h2>Filter & Pencarian</h2>
                    <div class="filter-controls">
                        <div class="search-box">
                            <input 
                                type="text" 
                                v-model="searchQuery" 
                                placeholder="Cari bahan ajar..."
                                class="search-input"
                            >
                            <span class="search-icon">🔍</span>
                        </div>
                        
                        <select v-model="selectedJenis" class="filter-select">
                            <option value="">Semua Jenis</option>
                            <option value="BMP">BMP</option>
                            <option value="Modul">Modul</option>
                        </select>
                        
                        <select v-model="sortBy" class="filter-select">
                            <option value="nama">Urutkan: Nama</option>
                            <option value="stok">Urutkan: Stok</option>
                            <option value="kode">Urutkan: Kode</option>
                        </select>
                        
                        <button @click="resetFilter" class="btn-reset">Reset</button>
                    </div>
                    
                    <div class="filter-info">
                        <span>Menampilkan {{ filteredBahanAjar.length }} dari {{ totalItems }} item</span>
                    </div>
                </section>
                
                <!-- Stok Statistics -->
                <section class="stats-section">
                    <div class="stats-grid">
                        <div class="stat-card">
                            <h3>{{ totalItems }}</h3>
                            <p>Total Item</p>
                        </div>
                        <div class="stat-card">
                            <h3>{{ totalStok }}</h3>
                            <p>Total Stok</p>
                        </div>
                        <div class="stat-card">
                            <h3>{{ lowStockItems }}</h3>
                            <p>Stok Rendah (&lt;50)</p>
                        </div>
                        <div class="stat-card">
                            <h3>{{ outOfStockItems }}</h3>
                            <p>Habis</p>
                        </div>
                    </div>
                </section>
                
                <!-- Bahan Ajar Grid -->
                <section class="bahan-ajar-section">
                    <h2>Daftar Bahan Ajar</h2>
                    
                    <div v-if="loading" class="loading">
                        <div class="spinner"></div>
                        <p>Sedang memuat data...</p>
                    </div>
                    
                    <div v-else-if="filteredBahanAjar.length === 0" class="no-data">
                        <p>😢 Tidak ada data yang ditemukan</p>
                        <button @click="resetFilter" class="btn-primary">Reset Filter</button>
                    </div>
                    
                    <div v-else class="bahan-ajar-grid">
                        <div 
                            v-for="bahan in paginatedBahanAjar" 
                            :key="bahan.kodeBarang"
                            class="bahan-ajar-card"
                            :class="{ 'low-stock': bahan.stok < 50, 'out-of-stock': bahan.stok === 0 }"
                        >
                            <div class="card-image">
                                <img :src="bahan.cover" :alt="bahan.namaBarang">
                                <div class="stock-badge" :class="getStockBadgeClass(bahan.stok)">
                                    {{ getStockStatus(bahan.stok) }}
                                </div>
                            </div>
                            
                            <div class="card-content">
                                <h3 class="card-title">{{ bahan.namaBarang }}</h3>
                                <div class="card-info">
                                    <p><strong>Kode:</strong> {{ bahan.kodeBarang }}</p>
                                    <p><strong>Edisi:</strong> {{ bahan.edisi }}</p>
                                    <p><strong>Lokasi:</strong> {{ bahan.kodeLokasi }}</p>
                                    <p><strong>Stok:</strong> 
                                        <span :class="getStockClass(bahan.stok)">
                                            {{ bahan.stok }} buah
                                        </span>
                                    </p>
                                </div>
                                
                                <div class="card-actions">
                                    <button 
                                        @click="viewDetails(bahan)" 
                                        class="btn-info"
                                        :disabled="bahan.stok === 0"
                                    >
                                        📋 Detail
                                    </button>
                                    <button 
                                        @click="orderBahanAjar(bahan)" 
                                        class="btn-order"
                                        :disabled="bahan.stok === 0"
                                        :class="{ 'disabled': bahan.stok === 0 }"
                                    >
                                        🛒 {{ bahan.stok === 0 ? 'Habis' : 'Pesan' }}
                                    </button>
                                </div>
                            </div>
                        </div>
                    </div>
                    
                    <!-- Pagination -->
                    <div v-if="totalPages > 1" class="pagination">
                        <button 
                            @click="currentPage--" 
                            :disabled="currentPage === 1"
                            class="btn-pagination"
                        >
                            ← Previous
                        </button>
                        
                        <span class="page-info">
                            Halaman {{ currentPage }} dari {{ totalPages }}
                        </span>
                        
                        <button 
                            @click="currentPage++" 
                            :disabled="currentPage === totalPages"
                            class="btn-pagination"
                        >
                            Next →
                        </button>
                    </div>
                </section>
                
                <!-- Modal Detail -->
                <div v-if="selectedBahan" class="modal-overlay" @click="closeModal">
                    <div class="modal-content" @click.stop>
                        <div class="modal-header">
                            <h3>Detail Bahan Ajar</h3>
                            <button @click="closeModal" class="close-btn">&times;</button>
                        </div>
                        <div class="modal-body">
                            <div class="detail-image">
                                <img :src="selectedBahan.cover" :alt="selectedBahan.namaBarang">
                            </div>
                            <div class="detail-info">
                                <h2>{{ selectedBahan.namaBarang }}</h2>
                                <div class="detail-grid">
                                    <div class="detail-item">
                                        <label>Kode Barang:</label>
                                        <span>{{ selectedBahan.kodeBarang }}</span>
                                    </div>
                                    <div class="detail-item">
                                        <label>Kode Lokasi:</label>
                                        <span>{{ selectedBahan.kodeLokasi }}</span>
                                    </div>
                                    <div class="detail-item">
                                        <label>Jenis:</label>
                                        <span>{{ selectedBahan.jenisBarang }}</span>
                                    </div>
                                    <div class="detail-item">
                                        <label>Edisi:</label>
                                        <span>{{ selectedBahan.edisi }}</span>
                                    </div>
                                    <div class="detail-item">
                                        <label>Stok Tersedia:</label>
                                        <span :class="getStockClass(selectedBahan.stok)">
                                            {{ selectedBahan.stok }} buah
                                        </span>
                                    </div>
                                </div>
                                
                                <div class="order-form">
                                    <h4>Form Pemesanan</h4>
                                    <div class="form-group">
                                        <label>Jumlah:</label>
                                        <input 
                                            type="number" 
                                            v-model.number="orderQuantity" 
                                            min="1" 
                                            :max="selectedBahan.stok"
                                            class="form-input"
                                        >
                                        <small>Maksimal: {{ selectedBahan.stok }} buah</small>
                                    </div>
                                    <div class="form-group">
                                        <label>Nama Pemesan:</label>
                                        <input 
                                            type="text" 
                                            v-model="ordererName" 
                                            placeholder="Masukkan nama lengkap"
                                            class="form-input"
                                            required
                                        >
                                    </div>
                                    <div class="form-group">
                                        <label>Email:</label>
                                        <input 
                                            type="email" 
                                            v-model="ordererEmail" 
                                            placeholder="email@example.com"
                                            class="form-input"
                                            required
                                        >
                                    </div>
                                    <div class="form-group">
                                        <label>Total Harga:</label>
                                        <div class="total-price">
                                            Rp {{ formatCurrency(orderQuantity * 50000) }}
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="modal-footer">
                            <button @click="closeModal" class="btn-cancel">Batal</button>
                            <button 
                                @click="confirmOrder" 
                                class="btn-confirm"
                                :disabled="!isOrderValid"
                            >
                                Konfirmasi Pesanan
                            </button>
                        </div>
                    </div>
                </div>
            </div>
        </main>
        
        <footer class="footer">
            <div class="container">
                <p>&copy; 2025 Universitas Terbuka. All rights reserved.</p>
            </div>
        </footer>
    </div>

    <script src="js/dataBahanAjar.js"></script>
    <script src="js/stok-app.js"></script>
</body>
</html>
```

### 🧠 **js/stok-app.js**
```javascript
new Vue({
    el: '#stok-app',
    data: {
        // Data dari dataBahanAjar.js
        bahanAjar: dataBahanAjar,
        
        // Filter dan Search
        searchQuery: '',
        selectedJenis: '',
        sortBy: 'nama',
        
        // Pagination
        currentPage: 1,
        itemsPerPage: 6,
        
        // Loading state
        loading: false,
        
        // Modal
        selectedBahan: null,
        orderQuantity: 1,
        ordererName: '',
        ordererEmail: '',
        
        // Order history
        orders: []
    },
    computed: {
        // Filter bahan ajar berdasarkan search dan filter
        filteredBahanAjar() {
            let filtered = this.bahanAjar;
            
            // Filter berdasarkan search query
            if (this.searchQuery) {
                const query = this.searchQuery.toLowerCase();
                filtered = filtered.filter(item => 
                    item.namaBarang.toLowerCase().includes(query) ||
                    item.kodeBarang.toLowerCase().includes(query) ||
                    item.kodeLokasi.toLowerCase().includes(query)
                );
            }
            
            // Filter berdasarkan jenis
            if (this.selectedJenis) {
                filtered = filtered.filter(item => item.jenisBarang === this.selectedJenis);
            }
            
            // Sorting
            filtered.sort((a, b) => {
                switch(this.sortBy) {
                    case 'nama':
                        return a.namaBarang.localeCompare(b.namaBarang);
                    case 'stok':
                        return b.stok - a.stok;
                    case 'kode':
                        return a.kodeBarang.localeCompare(b.kodeBarang);
                    default:
                        return 0;
                }
            });
            
            return filtered;
        },
        
        // Pagination
        paginatedBahanAjar() {
            const start = (this.currentPage - 1) * this.itemsPerPage;
            const end = start + this.itemsPerPage;
            return this.filteredBahanAjar.slice(start, end);
        },
        
        totalPages() {
            return Math.ceil(this.filteredBahanAjar.length / this.itemsPerPage);
        },
        
        // Statistics
        totalItems() {
            return this.filteredBahanAjar.length;
        },
        
        totalStok() {
            return this.filteredBahanAjar.reduce((total, item) => total + item.stok, 0);
        },
        
        lowStockItems() {
            return this.filteredBahanAjar.filter(item => item.stok > 0 && item.stok < 50).length;
        },
        
        outOfStockItems() {
            return this.filteredBahanAjar.filter(item => item.stok === 0).length;
        },
        
        // Order validation
        isOrderValid() {
            return this.orderQuantity > 0 && 
                   this.orderQuantity <= this.selectedBahan.stok &&
                   this.ordererName.trim().length >= 3 &&
                   this.isValidEmail(this.ordererEmail);
        }
    },
    methods: {
        // Stock status methods
        getStockStatus(stok) {
            if (stok === 0) return 'Habis';
            if (stok < 50) return 'Terbatas';
            return 'Tersedia';
        },
        
        getStockBadgeClass(stok) {
            if (stok === 0) return 'badge-out-of-stock';
            if (stok < 50) return 'badge-low-stock';
            return 'badge-in-stock';
        },
        
        getStockClass(stok) {
            if (stok === 0) return 'stock-out';
            if (stok < 50) return 'stock-low';
            return 'stock-normal';
        },
        
        // Modal methods
        viewDetails(bahan) {
            this.selectedBahan = bahan;
            this.orderQuantity = 1;
            this.ordererName = '';
            this.ordererEmail = '';
        },
        
        closeModal() {
            this.selectedBahan = null;
        },
        
        // Order methods
        orderBahanAjar(bahan) {
            this.viewDetails(bahan);
        },
        
        confirmOrder() {
            if (!this.isOrderValid) {
                this.showNotification('Mohon lengkapi form dengan benar!', 'error');
                return;
            }
            
            // Simulasi proses order
            const order = {
                id: Date.now(),
                kodeBarang: this.selectedBahan.kodeBarang,
                namaBarang: this.selectedBahan.namaBarang,
                quantity: this.orderQuantity,
                customerName: this.ordererName,
                customerEmail: this.ordererEmail,
                totalPrice: this.orderQuantity * 50000,
                orderDate: new Date().toISOString(),
                status: 'Diproses'
            };
            
            // Tambahkan ke orders
            this.orders.push(order);
            
            // Kurangi stok
            const bahanIndex = this.bahanAjar.findIndex(item => item.kodeBarang === this.selectedBahan.kodeBarang);
            if (bahanIndex !== -1) {
                this.bahanAjar[bahanIndex].stok -= this.orderQuantity;
            }
            
            // Simpan ke localStorage
            localStorage.setItem('sittaOrders', JSON.stringify(this.orders));
            
            // Tampilkan notifikasi
            this.showNotification(`Pesanan berhasil! ${order.namaBarang} (${order.quantity} buah)`, 'success');
            
            // Tutup modal
            this.closeModal();
        },
        
        // Utility methods
        resetFilter() {
            this.searchQuery = '';
            this.selectedJenis = '';
            this.sortBy = 'nama';
            this.currentPage = 1;
        },
        
        formatCurrency(amount) {
            return amount.toLocaleString('id-ID');
        },
        
        isValidEmail(email) {
            const emailPattern = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
            return emailPattern.test(email);
        },
        
        showNotification(message, type = 'info') {
            // Buat elemen notifikasi
            const notification = document.createElement('div');
            notification.className = `notification notification-${type}`;
            notification.textContent = message;
            
            // Style notifikasi
            Object.assign(notification.style, {
                position: 'fixed',
                top: '20px',
                right: '20px',
                padding: '1rem 1.5rem',
                borderRadius: '5px',
                color: 'white',
                fontWeight: 'bold',
                zIndex: '1000',
                transform: 'translateX(100%)',
                transition: 'transform 0.3s ease',
                maxWidth: '300px'
            });
            
            // Warna berdasarkan tipe
            const colors = {
                success: '#27ae60',
                error: '#e74c3c',
                warning: '#f39c12',
                info: '#3498db'
            };
            notification.style.backgroundColor = colors[type] || colors.info;
            
            // Tambahkan ke body
            document.body.appendChild(notification);
            
            // Animasi masuk
            setTimeout(() => {
                notification.style.transform = 'translateX(0)';
            }, 100);
            
            // Hapus setelah 3 detik
            setTimeout(() => {
                notification.style.transform = 'translateX(100%)';
                setTimeout(() => {
                    notification.remove();
                }, 300);
            }, 3000);
        }
    },
    watch: {
        // Watch untuk reset pagination saat filter berubah
        searchQuery() {
            this.currentPage = 1;
        },
        selectedJenis() {
            this.currentPage = 1;
        },
        sortBy() {
            this.currentPage = 1;
        },
        
        // Watch untuk order quantity validation
        orderQuantity(newVal) {
            if (newVal > this.selectedBahan?.stok) {
                this.orderQuantity = this.selectedBahan.stok;
            }
            if (newVal < 1) {
                this.orderQuantity = 1;
            }
        }
    },
    mounted() {
        // Load orders dari localStorage
        const savedOrders = localStorage.getItem('sittaOrders');
        if (savedOrders) {
            this.orders = JSON.parse(savedOrders);
        }
        
        // Simulasi loading
        this.loading = true;
        setTimeout(() => {
            this.loading = false;
        }, 1000);
    }
});
```

---

## 🧪 **Latihan Praktik Vue.js**

### ✅ **Latihan 1: Form Validation dengan Vue.js**
```html
<div id="validation-app">
    <h2>Form Pendaftaran</h2>
    <form @submit.prevent="submitForm">
        <div class="form-group">
            <label>Nama Lengkap:</label>
            <input 
                type="text" 
                v-model="form.nama" 
                @blur="validateNama"
                :class="{ 'error': errors.nama }"
            >
            <span v-if="errors.nama" class="error-message">{{ errors.nama }}</span>
        </div>
        
        <div class="form-group">
            <label>Email:</label>
            <input 
                type="email" 
                v-model="form.email" 
                @blur="validateEmail"
                :class="{ 'error': errors.email }"
            >
            <span v-if="errors.email" class="error-message">{{ errors.email }}</span>
        </div>
        
        <div class="form-group">
            <label>Umur:</label>
            <input 
                type="number" 
                v-model.number="form.umur" 
                @blur="validateUmur"
                :class="{ 'error': errors.umur }"
            >
            <span v-if="errors.umur" class="error-message">{{ errors.umur }}</span>
        </div>
        
        <div class="form-group">
            <label>Program Studi:</label>
            <select v-model="form.prodi" :class="{ 'error': errors.prodi }">
                <option value="">Pilih Program Studi</option>
                <option value="ti">Teknik Informatika</option>
                <option value="si">Sistem Informasi</option>
                <option value="mi">Manajemen Informatika</option>
            </select>
            <span v-if="errors.prodi" class="error-message">{{ errors.prodi }}</span>
        </div>
        
        <button type="submit" :disabled="!isFormValid">Daftar</button>
    </form>
    
    <div v-if="submitted" class="success-message">
        <h3>Form berhasil disubmit!</h3>
        <pre>{{ JSON.stringify(form, null, 2) }}</pre>
    </div>
</div>

<script>
new Vue({
    el: '#validation-app',
    data: {
        form: {
            nama: '',
            email: '',
            umur: '',
            prodi: ''
        },
        errors: {},
        submitted: false
    },
    computed: {
        isFormValid() {
            return Object.keys(this.errors).length === 0 &&
                   this.form.nama &&
                   this.form.email &&
                   this.form.umur &&
                   this.form.prodi;
        }
    },
    methods: {
        validateNama() {
            if (!this.form.nama) {
                this.$set(this.errors, 'nama', 'Nama wajib diisi');
            } else if (this.form.nama.length < 3) {
                this.$set(this.errors, 'nama', 'Nama minimal 3 karakter');
            } else {
                this.$delete(this.errors, 'nama');
            }
        },
        
        validateEmail() {
            const emailPattern = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
            if (!this.form.email) {
                this.$set(this.errors, 'email', 'Email wajib diisi');
            } else if (!emailPattern.test(this.form.email)) {
                this.$set(this.errors, 'email', 'Format email tidak valid');
            } else {
                this.$delete(this.errors, 'email');
            }
        },
        
        validateUmur() {
            if (!this.form.umur) {
                this.$set(this.errors, 'umur', 'Umur wajib diisi');
            } else if (this.form.umur < 17) {
                this.$set(this.errors, 'umur', 'Umur minimal 17 tahun');
            } else if (this.form.umur > 60) {
                this.$set(this.errors, 'umur', 'Umur maksimal 60 tahun');
            } else {
                this.$delete(this.errors, 'umur');
            }
        },
        
        validateProdi() {
            if (!this.form.prodi) {
                this.$set(this.errors, 'prodi', 'Program studi wajib dipilih');
            } else {
                this.$delete(this.errors, 'prodi');
            }
        },
        
        submitForm() {
            // Validasi semua field
            this.validateNama();
            this.validateEmail();
            this.validateUmur();
            this.validateProdi();
            
            if (this.isFormValid) {
                this.submitted = true;
                console.log('Form submitted:', this.form);
            }
        }
    },
    watch: {
        'form.nama'() {
            if (this.errors.nama) this.validateNama();
        },
        'form.email'() {
            if (this.errors.email) this.validateEmail();
        },
        'form.umur'() {
            if (this.errors.umur) this.validateUmur();
        },
        'form.prodi'() {
            if (this.errors.prodi) this.validateProdi();
        }
    }
});
</script>
```

### ✅ **Latihan 2: Shopping Cart dengan Vue.js**
```html
<div id="cart-app">
    <h2>🛒 Shopping Cart</h2>
    
    <!-- Product List -->
    <section class="products">
        <h3>Produk Tersedia</h3>
        <div class="product-grid">
            <div v-for="product in products" :key="product.id" class="product-card">
                <h4>{{ product.name }}</h4>
                <p class="price">Rp {{ formatCurrency(product.price) }}</p>
                <p class="stock">Stok: {{ product.stock }}</p>
                <div class="add-to-cart">
                    <input 
                        type="number" 
                        v-model.number="product.quantity" 
                        min="1" 
                        :max="product.stock"
                        :disabled="product.stock === 0"
                    >
                    <button 
                        @click="addToCart(product)" 
                        :disabled="product.stock === 0 || product.quantity === 0"
                    >
                        Tambah ke Keranjang
                    </button>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Cart -->
    <section class="cart">
        <h3>Keranjang Belanja ({{ cartItemCount }} item)</h3>
        
        <div v-if="cart.length === 0" class="empty-cart">
            <p>Keranjang belanja kosong</p>
        </div>
        
        <div v-else>
            <div class="cart-items">
                <div v-for="item in cart" :key="item.id" class="cart-item">
                    <div class="item-info">
                        <h4>{{ item.name }}</h4>
                        <p>Rp {{ formatCurrency(item.price) }} x {{ item.quantity }}</p>
                    </div>
                    <div class="item-actions">
                        <button @click="updateQuantity(item.id, item.quantity - 1)">-</button>
                        <span>{{ item.quantity }}</span>
                        <button @click="updateQuantity(item.id, item.quantity + 1)">+</button>
                        <button @click="removeFromCart(item.id)" class="remove-btn">🗑️</button>
                    </div>
                    <div class="item-total">
                        Rp {{ formatCurrency(item.price * item.quantity) }}
                    </div>
                </div>
            </div>
            
            <div class="cart-summary">
                <div class="summary-row">
                    <span>Subtotal:</span>
                    <span>Rp {{ formatCurrency(subtotal) }}</span>
                </div>
                <div class="summary-row">
                    <span>Pajak (10%):</span>
                    <span>Rp {{ formatCurrency(tax) }}</span>
                </div>
                <div class="summary-row total">
                    <span>Total:</span>
                    <span>Rp {{ formatCurrency(total) }}</span>
                </div>
            </div>
            
            <button @click="checkout" class="checkout-btn">Checkout</button>
        </div>
    </section>
</div>

<script>
new Vue({
    el: '#cart-app',
    data: {
        products: [
            { id: 1, name: 'Buku Pemrograman Web', price: 75000, stock: 10, quantity: 1 },
            { id: 2, name: 'Buku Database', price: 85000, stock: 5, quantity: 1 },
            { id: 3, name: 'Buku Algoritma', price: 65000, stock: 0, quantity: 1 },
            { id: 4, name: 'Buku Jaringan Komputer', price: 95000, stock: 8, quantity: 1 }
        ],
        cart: []
    },
    computed: {
        cartItemCount() {
            return this.cart.reduce((total, item) => total + item.quantity, 0);
        },
        subtotal() {
            return this.cart.reduce((total, item) => total + (item.price * item.quantity), 0);
        },
        tax() {
            return this.subtotal * 0.1;
        },
        total() {
            return this.subtotal + this.tax;
        }
    },
    methods: {
        addToCart(product) {
            if (product.quantity === 0 || product.stock === 0) return;
            
            const existingItem = this.cart.find(item => item.id === product.id);
            
            if (existingItem) {
                // Update quantity jika sudah ada di cart
                const newQuantity = existingItem.quantity + product.quantity;
                if (newQuantity <= product.stock) {
                    existingItem.quantity = newQuantity;
                } else {
                    alert(`Stok tidak mencukupi! Maksimal ${product.stock} buah`);
                }
            } else {
                // Tambah item baru ke cart
                this.cart.push({
                    id: product.id,
                    name: product.name,
                    price: product.price,
                    quantity: product.quantity,
                    maxStock: product.stock
                });
            }
            
            // Reset quantity input
            product.quantity = 1;
            
            // Update stock
            product.stock -= product.quantity;
        },
        
        updateQuantity(productId, newQuantity) {
            const item = this.cart.find(item => item.id === productId);
            const product = this.products.find(p => p.id === productId);
            
            if (newQuantity <= 0) {
                this.removeFromCart(productId);
            } else if (newQuantity <= item.maxStock) {
                const quantityDiff = newQuantity - item.quantity;
                item.quantity = newQuantity;
                product.stock -= quantityDiff;
            } else {
                alert(`Maksimal ${item.maxStock} buah`);
            }
        },
        
        removeFromCart(productId) {
            const itemIndex = this.cart.findIndex(item => item.id === productId);
            const product = this.products.find(p => p.id === productId);
            
            if (itemIndex !== -1) {
                const item = this.cart[itemIndex];
                product.stock += item.quantity;
                this.cart.splice(itemIndex, 1);
            }
        },
        
        checkout() {
            if (this.cart.length === 0) return;
            
            alert(`Checkout berhasil! Total: Rp ${this.formatCurrency(this.total)}`);
            this.cart = [];
        },
        
        formatCurrency(amount) {
            return amount.toLocaleString('id-ID');
        }
    }
});
</script>
```

---

## 📋 **Tugas Praktik 2**

### 🎯 **Kriteria Penilaian**

1. **Arsitektur dan Struktur Proyek Vue.js (5 poin)**
   - Struktur folder yang rapi dan terorganisir
   - Penamaan file yang konsisten
   - Pemisahan concern yang baik

2. **Data Binding & Directive untuk List Rendering (20 poin)**
   - Penggunaan mustaches, v-text, v-html yang tepat
   - Implementasi v-bind dan v-model yang benar
   - List rendering dengan v-for yang efektif

3. **Penggunaan Conditional (10 poin)**
   - Implementasi v-if, v-else, v-else-if yang efektif
   - Penggunaan v-show yang tepat
   - Logika conditional yang sesuai kebutuhan

4. **Penggunaan Property (Computed/Methods) (10 poin)**
   - Computed properties untuk perhitungan
   - Methods untuk aksi dan fungsi
   - Penggunaan yang sesuai dan efisien

5. **Watchers (10 poin)**
   - Minimal 2 watcher untuk memantau perubahan data
   - Implementasi watcher yang relevan
   - Deep watcher jika diperlukan

6. **Formulir Input dan Validasi (20 poin)**
   - Form yang interaktif dan user-friendly
   - Validasi input yang komprehensif
   - Feedback yang jelas untuk user

7. **Kreativitas (10 poin)**
   - Interface yang menarik dan mudah digunakan
   - Fitur tambahan yang inovatif
   - User experience yang baik

8. **Penjelasan Video (15 poin)**
   - Durasi maksimal 15 menit
   - Penjelasan sistematika dan alur berpikir
   - Demonstrasi implementasi Vue.js

---

## 🎯 **Kesimpulan**

Pada pertemuan ini kita telah mempelajari:

### ✅ **Konsep Dasar Vue.js**
- Progressive framework yang mudah dipelajari
- Struktur aplikasi Vue yang terorganisir
- Konsep reaktivitas data

### ✅ **Data Binding**
- One-way data binding dengan mustaches dan directives
- Two-way data binding dengan v-model
- Dynamic binding dengan v-bind

### ✅ **Conditional Rendering**
- v-if, v-else-if, v-else untuk conditional rendering
- v-show untuk toggle visibility
- Perbedaan dan penggunaan yang tepat

### ✅ **Computed Properties dan Methods**
- Computed properties untuk perhitungan yang di-cache
- Methods untuk fungsi dan aksi
- Perbedaan dan penggunaan yang optimal

### ✅ **Watchers**
- Basic watcher untuk memantau perubahan data
- Deep watcher untuk nested objects
- Implementasi watcher yang efektif

### ✅ **Studi Kasus Aplikasi Stok**
- Implementasi semua konsep Vue.js
- Form validation yang komprehensif
- Shopping cart functionality
- Local storage integration

---

## 📚 **Referensi Pembelajaran**

### 📖 **Dokumentasi Resmi**
- [Vue.js Official Documentation](https://vuejs.org/v2/guide/)
- [Vue.js API Reference](https://vuejs.org/v2/api/)
- [Vue.js Style Guide](https://vuejs.org/v2/style-guide/)

### 🎥 **Video Tutorial**
- [Vue.js Crash Course](https://www.youtube.com/watch?v=nhBVL41-_Cw)
- [Vue.js Tutorial for Beginners](https://www.youtube.com/playlist)

### 📚 **Artikel dan Tutorial**
- [Vue.js Tutorial](https://www.tutorialspoint.com/vuejs/index.htm)
- [Vue.js Examples](https://vuejs.org/v2/examples/)

---

## 🚀 **Persiapan Pertemuan Selanjutnya**

Pertemuan 14 akan membahas:
- **Vue.js Component dan Template**
- **Array Processing dengan v-for**
- **Filter untuk Formatting Data**
- **Event Handling**
- **Studi Kasus: Aplikasi Tracking dengan Vue Component**

**Persiapan:**
- Pelajari konsep component-based architecture
- Pahami konsep props dan events
- Baca dokumentasi Vue.js components

---

**Selamat belajar dan semoga sukses! 🎉**

*Universitas Terbuka - Program Studi Sistem Informasi*
